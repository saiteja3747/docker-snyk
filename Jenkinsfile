node {
    stage('Preparation') {
        git 'https://github.com/saiteja3747/docker-snyk.git'
    }
    stage('install'){
        sh 'npm install' // Dependency Installation stage
    }
    stage('Scan') {
        snykSecurity organisation: '', projectName: 'nodejs-demo-snyk', severity: 'medium', snykInstallation: 'Snyk', snykTokenId: '74285fbf-bad6-479c-9c3a-707290bbcdf9', targetFile: 'package.json'
    }
    stage('Build') {
        echo "Build"
    }
    stage('Results') {
        echo "Test Result"
    }
}
