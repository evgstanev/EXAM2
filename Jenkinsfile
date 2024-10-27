pipeline {
    agent any
    when  {
      branch 'feature-ci-pipeline'
    }
    stages {
        stage('Restore  dependencies') {
            steps {
                sh 'dotnet build'
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
