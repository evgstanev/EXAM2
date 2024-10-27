pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            when {
                branch 'feature-ci-pipeline'
            }
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Build Project') {
            steps {
                sh 'dotnet build'
            }
        }
        stage('Execute test') {
            steps {
                sh 'dotnet test'
            }
        }
    }
}
