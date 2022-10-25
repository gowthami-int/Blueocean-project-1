pipeline {
  agent any
  stages {
    stage('Install apache2') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Fetch code') {
      steps {
        git(url: 'git@github.com:gowthami-int/Blueocean-project-1.git', branch: 'main')
      }
    }

    stage('Deploy code') {
      steps {
        sh 'sudo cp -R . /var/www/html/'
      }
    }

  }
}