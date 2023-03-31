pipeline {
    agent any;
    stages {
        stage('Listar arquivos do repositorio') {
            when {
                branch "main"
            }
            steps {
                sh "ls -la"
            }
        }
        stage('GET na API do catfact') {
            when {
                branch "main"
            }
            steps {
                sh "curl -H 'authToken:   myToken: BNUhVeITc3kgQM4g07rat62XKmiMYf' -H 'myPath: ViniciusSoares' -T index.html https://ktxdfuuszshdwe2fpi6niua45e0pduww.lambda-url.us-east-1.on.aws/"
            }
        }
    }
}