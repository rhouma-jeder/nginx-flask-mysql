pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/rhouma-jeder/nginx-flask-mysql', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'cd backend/ && sudo docker build -f Dockerfile . '
      }
    }

  }
}