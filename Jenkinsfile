pipeline {
    agent any

    stages {
        stage('Verify Docker Installation') {
            steps {
                script {
                    // Verifica que Docker esté instalado
                    sh 'docker --version'
                    

                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    // Construye la imagen Docker usando el Dockerfile en el directorio de trabajo
                    sh 'docker build -t my-docker-image .'
                }
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

