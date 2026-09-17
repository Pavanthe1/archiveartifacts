pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Updated with your new repository path
                git branch: 'main', url: 'https://github.com/Pavanthe1/archiveartifacts.git'
            }
        }
        stage ('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
