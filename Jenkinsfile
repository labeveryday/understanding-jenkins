pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'python -m pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}