pipeline {
  agent {
    node {
      label 'node1'
    }

  }
  stages {
    stage('Build Phase') {
      steps {
        sh 'echo "Building..."'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh '''echo "Testing..."
sleep 10'''
          }
        }
        stage('TestA') {
          steps {
            sh 'echo "TestingA..."'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
      }
    }
  }
}
