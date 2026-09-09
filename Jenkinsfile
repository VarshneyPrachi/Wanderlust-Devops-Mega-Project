pipeline {
    agent { label 'windows-agent' }

    stages {

        stage('Test Agent') {
            steps {
                echo 'Hello from Wanderlust Jenkins CI!'
                bat 'java -version'
                bat 'node --version'
                bat 'npm --version'
            }
        }

        stage('Check Workspace') {
            steps {
                bat 'echo Jenkins workspace: %CD%'
                bat 'dir'
            }
        }

        stage('Test Docker') {
            steps {
                bat 'docker --version'
            }
        }

        stage('Success') {
            steps {
                echo 'Wanderlust-CI basic Jenkins test completed successfully!'
            }
        }
    }
}