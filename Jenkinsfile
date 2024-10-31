pipeline {
    agent any
    stages {
        stage('Clonar repositorio') {
            steps {
                git ' https://github.com/jorgeluisculisvillugas/Jenkinsfile.git'
            }
        }
        stage('Construir aplicación') {
            steps {
                // En Windows usamos "bat" y llamamos al script de Maven con ".cmd"
                bat './mvnw.cmd clean package'
            }
        }
        stage('Ejecutar aplicación') {
            steps {
                // Usamos "bat" en lugar de "sh" para ejecutar el JAR en Windows
                bat 'java -jar target/gestion-musica-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}

