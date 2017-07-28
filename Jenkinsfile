pipeline {
  agent {
    docker {
      image 'arg'
      args '-u root -v /var/run/docker.sock:/var/run/docker.sock'
    }
    
  }
  stages {
    stage('create-docker-image') {
      steps {
        sh '''docker run -d -it -p 8811:80 -v /var/www/html:/var/www/app/public_html/  naqoda/centos-apache-php

'''
      }
    }
    stage('dg') {
      steps {
        sh 'docker build -t  -f Dockerfile .'
      }
    }
  }
}