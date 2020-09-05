pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building the java code operation'
            echo "Get path from ${chromdriverpath}"
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying app'
      }
    }

  }
  environment {
    chromdriverpath = 'c:/'
  }
}
