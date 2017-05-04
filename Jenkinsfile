pipeline {
  agent {
    node {
      label 'maser'
    }
    
  }
  stages {
    stage('Prep') {
      steps {
        parallel(
          "Prep": {
            sh 'echo "Prepare Server for Checkout"'
            
          },
          "Prep-1": {
            sh 'echo "Prep-1"'
            
          }
        )
      }
    }
    stage('Build') {
      steps {
        sh '''mvn -V

&& mvn clean install'''
      }
    }
  }
}