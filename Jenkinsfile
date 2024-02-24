pipeline {
    agent any

    environment {
        DOCKER_USERNAME = credentials('DOCKER_USERNAME')
        PYTHONPATH = '/usr/lib/python3.11'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                script {
                    sh "echo 'DOCKER_USERNAME=${DOCKER_USERNAME}' > .env"
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying......'
                script {
                    // Run Ansible playbook
                    sh "docker --version"
                    sh "ansible-playbook --version"
                }
            }
        }
    }
}
