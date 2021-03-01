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

    stage('Deploy') {
      steps {
        echo 'deploying'
        sh 'java -Dserver.port=8082 jar target/spring petclinic 2.3.1.BUILD SNAPSHOT.jar'
      }
    }

  }
}