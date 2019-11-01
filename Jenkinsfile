pipeline {
  agent {
    docker {
      image 'node:10-alpine'
      args '-v /Users/jean-marcelbelmont/jenkins_data'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''node --version

npm install'''
      }
    }
    stage('Cucumber Tests') {
      steps {
        sh 'npm run acceptance:tests'
      }
    }
    stage('') {
      steps {
        sh 'curl \'https://download.jboss.org/wildfly/18.0.0.Final/wildfly-18.0.0.Final.zip\' -H \'Connection: keep-alive\' --compressed'
      }
    }
  }
}