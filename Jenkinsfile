pipeline {
    agent { docker 'node:dubnium-alpine3.11' }
    stages {
        stage ('Checkout') {
          steps {
            git 'https://github.com/liorbenami1/the-example-app.nodejs.git'
          }
        }
        stage('Build') {
            steps {
                sh 'echo Hello'
                //sh 'mvn clean package'
                //junit '**/target/surefire-reports/TEST-*.xml'
                //archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
    }
}
