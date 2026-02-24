pipeline {
    agent any

    stages {
        stage('checkout from git') {
            steps {
             checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'Kalyan_Cred', url: 'https://github.com/kalyansagar5/node-telegram-bot-api.git']])
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('run script') {
            steps {
                sh 'npm run build'
            }
        }
        
    }
}
