pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''npm install'''
            }
        }

        stage('Testes') {
            steps {
                sh '''npm test'''
            }
        }
    }

    post {
        success {
            echo 'Os testes foram executados com sucesso!'
        }
        failure {
            echo 'Os testes falharam'
        }
    }
}