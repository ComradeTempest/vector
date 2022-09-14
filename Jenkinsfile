pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                git credentialsId: '20eabf2e-aef7-4367-b7ea-4d6222f93fe5', 
                url: 'git@github.com:ComradeTempest/vector.git',
                branch: 'main'
            }
        }
        stage('test') {
            steps {
                sh 'molecule test'
            }
        }
    }
}