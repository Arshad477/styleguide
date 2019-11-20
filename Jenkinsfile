pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-v /Users/477465/.m2'
    }

  }
  stages {
    stage('Intialize') {
      steps {
        sh 'echo "Intialize"'
      }
    }

    stage('Build') {
      steps {
        sh '''echo PATH = ${PATH}
echo M2_HOME = ${M2_HOME}
mvn clean
docker -v'''
      }
    }

  }
}