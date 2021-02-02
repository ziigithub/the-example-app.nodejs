pipeline {
    agent { docker 'node:dubnium-alpine3.11' }
    stages {
        stage ('Checkout') {
          steps {
            git \
            branch: 'liorbenami_branch', \
            url: 'https://github.com/liorbenami1/the-example-app.nodejs.git'
          }
        }
        stage('Build') {
            steps {
                //sh 'cd the-example-app.nodejs'
                sh 'npm install'
                //sh 'npm run start:dev'
                //sh 'mvn clean package'
                //junit '**/target/surefire-reports/TEST-*.xml'
                //archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                sh 'echo Hello'
                
            }
        }
        stage('Deploy-to-DEV') {
            steps {
                sh 'echo Hello'
                
            }
        }
    }
}
