@Library('Roboshop-shared-libary') _

pipeline {
    agent { label 'WS' }
    stages {           ///
        stage('Lint Checks') {
            steps {
                   script {
                       sample.info("message")
                  }
              sh "echo Installing Jslint"
              sh "npm i jslint"
              sh "node_modules/jslint/bin/jslint.js server.js || true"
            }         /////
        }
        stage ('Code Compile') {
            steps{
                sh "npm install"
            }
        }
    }
}