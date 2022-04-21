pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                echo 'chking outt'
                git branch: 'main', credentialsId: 'Deekshith112', url: 'https://github.com/Deekshith112/Mainmaster.git'
            }
        }
        stage('paybook execution') {
            steps {
                echo 'executing playbook'
                ansiblePlaybook credentialsId: 'Deekshith', disableHostKeyChecking: true, installation: 'ansible1', inventory: 'inventory.ini', playbook: 'playbook.yml'
            }
        }
    }
}
