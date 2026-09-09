pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'cat index.html'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'grep -q "DevOps" index.html'
                echo 'Test passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to Nginx...'
                sh 'sudo cp index.html /var/www/html/index.html'
                echo 'Deployment completed successfully!'
            }
        }
    }
}
