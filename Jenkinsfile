pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 2) {
          sh 'echo "Run nummer 1000"'
        }

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
        input(message: 'Are you sure to deploy?', ok: 'Yes, I am sure')
        echo 'Deployment completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build completed successfully'
      }
    }

  }
}