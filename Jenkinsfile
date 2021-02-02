pipeline {
    agent { 
        docker {
            //image 'node:dubnium-alpine3.11'
            image 'node:9'
            args '-p 3000:3000'
        }
        //docker 'node:dubnium-alpine3.11' 
      }
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
                sh 'npm install -g contentful-cli'
                sh 'npm install'
                sh 'npm run start:dev &'
                //sh 'mvn clean package'
                //junit '**/target/surefire-reports/TEST-*.xml'
                //archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
        stage('unit-test') {
            steps {
                sh 'npm run test:unit'
                sh 'sleep 5m'
            }
        }
        stage('Deploy-to-DEV') {
            steps {
                sh 'echo Hello'
                
            }
        }
    }
}
