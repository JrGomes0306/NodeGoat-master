pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Testes') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        successo {
            echo 'Os testes foram executados com sucesso!'
        }
        falhou {
            echo 'Os testes falharam'
        }
    }
}