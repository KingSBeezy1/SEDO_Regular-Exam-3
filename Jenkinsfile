pipeline {
    agent any
    stages {
        stage('Restore .NET Packages') {
            steps {
                bat 'dotnet restore' // For Windows, otherwise use 'sh' to execute the command
            }
        }

        stage('Build .NET Packages') {
            steps {
                bat 'dotnet build --no-restore' // For Windows, otherwise use 'sh' to execute the command
            }
        }

        stage('Run Unit and Integration Tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal' // For Windows, otherwise use 'sh' to execute the command
            }
        }
    }
}