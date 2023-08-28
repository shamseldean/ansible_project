pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Ansible Playbook') {
            steps {
                sh 'ansible-playbook playbook.yaml'
            }
        }
    }
}
