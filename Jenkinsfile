node {
    stage('Preparation') {
        git '<GITHUB REPO URL>'
    }
    stage('install'){
        sh 'npm install' // Dependency Installation stage
    }
    stage('Scan') {
        snykSecurity organisation: '', projectName: 'nodejs-demo-snyk', severity: 'medium', snykInstallation: 'Snyk', snykTokenId: '', targetFile: 'package.json'
    }
    stage('Build') {
        echo "Build"
    }
    stage('Results') {
        echo "Test Result"
    }
}
