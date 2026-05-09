pipeline {
    agent any

    environment {
        EMAIL = "dc3714107@gmail.com"
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
                    subject: "Build Success - Jenkins",
                    body: "Your build has been triggered successfully from GitHub webhook!",
                    to: "${EMAIL}"
                )
            }
        }
    }
}