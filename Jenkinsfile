pipeline {
  agent any
  stages {
    stage('create-docker-image') {
      steps {
        sh 'docker run -d -it -p 8811:80 -v /var/www/html:/var/www/app/public_html/  naqoda/centos-apache-php'
      }
    }
  }
}