pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building java application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
            echo "Chrome driver path ${ChromeDriverPath}"
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app to AWS server'
        input(message: 'Want to deploy?', id: 'Ok')
      }
    }

  }
  environment {
    ChromeDriverPath = 'C:\\Driver\\Path'
  }
}