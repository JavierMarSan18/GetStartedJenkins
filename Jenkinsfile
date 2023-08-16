pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'npm test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Aquí podrías implementar el despliegue a un servidor web o un servicio de hosting
                    echo 'Deploying to production...'
                }
            }
        }
    }

    post {
        always {
            // Limpia cualquier recurso temporal creado durante el proceso
            deleteDir()
        }
    }
}
