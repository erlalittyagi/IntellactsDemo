pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'mvn clean install'
            
          },
          "code quality": {
            sh 'sonar-scanner'
            
          }
        )
      }
    }
  }
}