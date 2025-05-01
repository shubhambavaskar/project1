pipeline {
  agent any

  stages {
    stage('Clone Code') {
      steps {
        git 'https://github.com/shubhambavaskar/index.html.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t shubham-web:v1 .'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run -d -p 8085:80 --name shubham-web shubham-web:v1 || true'
      }
    }
  }
}

