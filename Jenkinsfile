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
        input(message: 'Want to deploy?', id: 'Ok')
        echo 'Deploying the app to AWS server'
      }
    }

  }
  environment {
    ChromeDriverPath = 'C:\\Driver\\Path'
  }
}