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
            writeFile(file: 'logtest.txt', text: 'This automated log file')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            input 'Do you proceed with deployment?'
            echo 'Deploying app'
          }
        }

        stage('Artifcat') {
          steps {
            archiveArtifacts(artifacts: 'logtest.txt', allowEmptyArchive: true)
          }
        }

      }
    }

  }
  environment {
    chromdriverpath = 'c:/'
  }
}