pipeline {
    agent any
    stages {
        stage('excutable playbook') {
            steps {
                ansiblePlaybook credentialsId: 'ssh-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/var/lib/jenkins/workspace/project-ansible/inventory', playbook: '/var/lib/jenkins/workspace/project-ansible/playbook.yaml'
            }
        }
        // stage('Deploy to Remote Server') {
        //     steps {
        //         script {
        //             sshagent(credentials: ['b75b7baf-7b1f-4b16-98fe-d445003e4094']) {
        //                 sh """
        //                     ssh -i "shams-key-pair.pem" ubuntu@ec2-18-117-105-151.us-east-2.compute.amazonaws.com
        //                 """
        //             }
        //         }
        //     }
        // }
        // stage('Ansible Playbook') {
        //     steps {
        //         sh 'ansible-playbook playbook.yaml'
        //     }
        // }
    }
}
