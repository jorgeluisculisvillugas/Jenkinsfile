      pipeline {
          agent any
          stages {
              stage('Clonar repositorio') {
                  steps {
                      git 'https://github.com/jorgeluisculisvillugas/Jenkinsfile.git'
                  }
              }
              stage('Construir aplicación') {
                  steps {
                      sh './mvnw clean package'
                  }
              }
              stage('Ejecutar aplicación') {
                  steps {
                      sh 'java -jar target/gestion-musica-0.0.1-SNAPSHOT.jar'
                  }
              }
          }
      }
