pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                script {
                    echo 'Installing Node.js version 22'
                    sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | bash -'
                    sh 'apt-get install -y nodejs'
                    sh 'node -v'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Simulating build process by showing npm version'
                    sh 'npm -v'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Simulating test process'
                    sh 'echo JENKINS_URL is $JENKINS_URL'
                }
            }
        }
    }
}
