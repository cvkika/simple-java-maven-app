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
          sh 'mvn clean install -Denforcer.skip=true'
            }
   }
 }
}
            
