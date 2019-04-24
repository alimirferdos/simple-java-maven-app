pipeline {
  agent {
    node {
      label 'master'
    }
  }
  tools{
      maven "mvn"
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}
