pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from the repo
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // For static HTML, "build" could just be a validation or no-op
                echo 'Building static site...'
                // You could add linting or validation here if needed
            }
        }

        stage('Archive') {
            steps {
                // Archive the HTML files for later use
                archiveArtifacts artifacts: '**/*.html', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                // Example deploy step - adjust based on your environment
                echo 'Deploying the HTML files...'
                // For example, copy files to a web server or storage location
                // sh 'scp -r * user@yourserver:/var/www/html/'
            }
        }
    }
}
