pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        git(url: 'git@github.com:maddy3012/devops-bo.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy application') {
      steps {
        sh 'sudo apt cp -R * /var/www/html/'
      }
    }

  }
}