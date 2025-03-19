pipeline {
  agent none
  stages {
    stage('Test') {
      agent {
        kubernetes {
          yamlFile 'nodejs-pod.yaml'
        }
      }
      steps {
        container('maven') {
          echo 'Hello World!'   
          sh 'mvn --version'
        }
      }
    }
  }
}
