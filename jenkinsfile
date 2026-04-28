pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/cht-houdayfa/interactive-site.git'
      }
    }

    stage('Deploy') {
      steps {
        sh '''
        sudo rm -rf /var/www/html/*
        sudo cp -r * /var/www/html/
        '''
      }
    }
  }
}
