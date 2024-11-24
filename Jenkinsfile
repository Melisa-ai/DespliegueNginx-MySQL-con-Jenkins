pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                script {
                    // Clonar repositorio de código
                    git 'https://github.com/Melisa-ai/DespliegueNginx-MySQL-con-Jenkins.git'
                    
                    // Instalar dependencias
                    sh 'npm install'
                    
                    // Desplegar la aplicación
                    sh 'npm start'
                    
                    // Reiniciar el servidor web si es necesario
                    sh 'systemctl restart nginx'
                }
            }
        }
    }
}
