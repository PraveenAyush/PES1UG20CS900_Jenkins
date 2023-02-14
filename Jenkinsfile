pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o newfile newfile.cpp'
      }
    }
    stage('Test') {
      steps {
        sh './newfile'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  
  post {
    failure {
        echo 'Pipeline failed'
    }
  }
}
