pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Prepare') {
            steps {
                sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | bash -'
                sh 'apt-get update && apt-get install -y nodejs'
                sh 'node --version && npm --version' // Перевіримо встановлення
            }
        }

        stage('Build') {
            steps {
                sh 'npm install' // Встановлюємо залежності
                sh 'npm run build' // Запускаємо збірку
            }
        }

        stage('Test') {
            steps {
                sh 'npm test' // Запускаємо тести
                echo "JENKINS_URL is: ${env.JENKINS_URL}"
            }
        }
    }
}
