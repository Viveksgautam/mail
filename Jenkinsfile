pipeline {
    agent any

    environment {
        EMAIL = "vivekgautam14216@gmail.com"
    }

    stages {
        
        stage('Build') {
            steps {
                echo 'Triggered from GitHub webhook!'
            }
        }

        stage('Send Email Notification') {
            steps {
               emailext(
                subject: "NestJS App Deployed Successfully on EC2!",
                body: "Your Nest JS app is Deployed!/",
                to: "${EMAIL}"
               )
            }
        }

    }
}
