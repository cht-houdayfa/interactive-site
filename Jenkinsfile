pipeline {
  agent any

  stages {
    stage('Deploy') {
      steps {
        sh '''
          echo "Starting deployment..."
          sudo rm -rf /var/www/html/*
          sudo cp -r . /var/www/html/
          echo "Deployment completed successfully."
        '''
      }
    }
  }

  post {
    success {
      echo '✅ Pipeline executed successfully'
    }
    failure {
      echo '❌ Pipeline failed'
    }
  }
}
