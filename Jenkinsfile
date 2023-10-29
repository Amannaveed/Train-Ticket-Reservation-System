pipeline {
agent { label 'slave' }
stages {
  stage('git checkout') {
    steps {
    git 'https://github.com/Amannaveed/Train-Ticket-Reservation-System.git'
    }
  }

  stage('mvn cleaninstall') {
    steps {
     sh 'mvn clean install'
    }
  }

  stage('deploy') {
    steps {
       sh ''' sudo cp /home/ubuntu/jenkins/workspace/trainticket/target/*.war /opt/tomcat/apache-tomcat-9.0.68/webapps '''
    }
  }

}

}
