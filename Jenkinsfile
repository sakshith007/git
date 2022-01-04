pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/sakshith007/git.git'
            }
        }
        stage('Execute ansible') {
            steps {
                ansiblePlaybook credentialsId: 'srustik', disableHostKeyChecking: true, installation: 'ansible-2.9.6', inventory: 'hosts', playbook: 'win.yml'
            }
        }
    }
}

