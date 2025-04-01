pipeline {
    agent any
    stages {
        
        stage('Prepare') {
            steps {
        script {
            node {
                checkout scm
            }
        }
    }
            steps {
                sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -'
                sh 'sudo apt install -y nodejs'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'npm --version'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "JENKINS_URL is: ${env.JENKINS_URL}"
                }
            }
        }
    }
}
