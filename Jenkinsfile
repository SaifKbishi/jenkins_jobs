pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from Git repository
                git branch: 'main', url: 'https://github.com/example/repo.git'
            }
        }

        stage('Build') {
            steps {
                // Run build commands
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run unit tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy application (example: copy files to server)
                sh 'scp target/myapp.jar user@server:/opt/apps/'
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed. Please check logs.'
        }
    }
}
