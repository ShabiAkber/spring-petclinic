pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        echo 'compile the code'
        sh './mvnw compile'
      }
    }

    stage('Test') {
      steps {
        echo 'testing'
        sh './mvnw test'
      }
    }

    stage('Install Packages') {
      steps {
        echo 'installing packages into the code'
        sh './mvnw package'
      }
    }

  }
}