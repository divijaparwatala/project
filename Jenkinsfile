pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your git repo
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'No build needed for static HTML'
                // If you want, add simple checks here, like listing files
                sh 'dir'  // for Windows agents
                // or 'ls -la' for Linux agents
            }
        }

        stage('Test') {
            steps {
                echo 'No tests to run for static HTML'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying HTML file...'
                // Example: archive the HTML file as build artifact
                archiveArtifacts artifacts: '**/*.html', fingerprint: true
                // Or add commands to copy/deploy your HTML to server
            }
        }
    }
}
