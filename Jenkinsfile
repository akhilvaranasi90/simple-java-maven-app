pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building maven job'
        sh 'mvn clean install'
      }
    }
  }
}