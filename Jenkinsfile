pipeline {
    agent { label 'master' }
    environment {
          HOME = '.'
     }

     stages {
          stage('Source') {
               steps {
                    git branch: 'main',
                        url:    'https://github.com/NutthanichN/atm-web-frontend.git'
               }
          }
          stage('Build') {
               steps {
                    //sh 'mvn compile'
                    echo 'building...'
               }
          }
          stage('Test') {
               steps {
                    //sh 'mvn test'
                    echo 'testing...'
               }
          }
          stage('Deploy') {
               steps {
                    bat 'mvn spring-boot:run'
               }
          }
     }
}
