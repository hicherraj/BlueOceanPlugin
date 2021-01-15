pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Running Test 2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment completed'
      }
    }

  }
}