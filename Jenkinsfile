pipeline {
  agent none
  
  stages {
    stage ('Maven install') {
      agent {
        docker {
          image 'maven:latest'
              }
            }
      steps {
          sh 'mvn clean install'
            }
   }
    stage ('Build image') {
      agent any
      steps {
        sh 'docker build -t myapp:latest .'
      }
    }
 }
}
            
