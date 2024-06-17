pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/kendermag/curriculum-app', branch: 'master')
      }
    }

    stage('Log') {
      steps {
        sh '''ls -la
pwd'''
      }
    }

  }
}