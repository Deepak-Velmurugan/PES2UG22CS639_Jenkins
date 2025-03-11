pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG22CS639-1'
        sh 'g++ min.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
