pipeline {
    agent any

    stages {

        stage('Checkout Source') {
            steps {
                echo 'Source code fetched successfully.'
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo mkdir -p /var/www/html
                sudo cp index.html /var/www/html/
                sudo cp style.css /var/www/html/
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                sh 'ls -l /var/www/html'
                echo 'Website deployed successfully.'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline Completed Successfully!'
        }

        failure {
            echo 'Pipeline Failed!'
        }
    }
}
