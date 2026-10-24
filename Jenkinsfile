pipeline {
    agent any

    stages {
        stage("Restore dependencies") {
            when {
                branch "main"
            }
            steps {
                bat "dotnet restore" // Restore dependencies for Windows machines
            }
        }

        stage("Build the project") {
            when {
                branch "main"
            }
            steps {
                bat "dotnet build --no-restore" // Build the project for Windows machines
            }
        }

        stage("Run tests") {
            when {
                branch "main"
            }
            steps {
                bat "dotnet test --no-build --verbosity normal" // Run all tests for Windows machines
            }
        }
    }
}