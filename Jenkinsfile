pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/kendermag/curriculum-app', branch: 'master')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh '''ls -la
pwd'''
          }
        }

        stage('Front end unit test') {
          steps {
            sh '''cd curriculum-front && npm i && npm run test:unit
'''
          }
        }

      }
    }

  }
}