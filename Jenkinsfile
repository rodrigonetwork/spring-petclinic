pipeline {
  agent {
    docker {
      image 'openjdk:8-jdk'
      args '-p 9000:8080'
    }

  }
  stages {
    stage('java') {
      steps {
        sh 'echo $JAVA_HOME'
        sh 'pwd'
        sh './mvnw verify'
      }
    }
    stage('run') {
      steps {
        sh './mvnw spring-boot:run'
      }
    }
  }
}