pipeline {
  agent any
  tools{
    maven 'maven-3'
    jdk 'Java-8'
  }
  stages {
    stage('Pipeline Test') {
      steps {
        echo 'Building maven job'
      }
    }
    stage('Maven Test'){
      steps {
        sh '''
      echo "PATH = ${PATH}"
      echo "M2_HOME = ${M2_HOME}"
      '''
      }
    }
    stage('Build'){
    steps{
    sh 'mvn clean install -DskipTest=true'
    }
    }
    stage('Test'){
    steps{
    sh 'mvn clean test'
    }
    }
  }
}
