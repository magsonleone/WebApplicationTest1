pipeline {
    agent any
    stages {
        stage('Restore') {
            steps {
                script {
                    sh 'dotnet restore'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'dotnet build --configuration Release --no-restore'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'dotnet test --no-restore'
                }
            }
        }
        stage('Publish') {
            steps {
                script {
                    sh 'dotnet publish --configuration Release --no-restore --output ./publish'
                }
            }
        }
        stage('Deploy to Azure') {
            steps {
                script {
                    // Adicione aqui o comando ou script para deploy no Azure
                }
            }
        }
    }
}
