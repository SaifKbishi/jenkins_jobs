pipeline {
    agent any

    stages {
        stage('Greeting') {
            steps {
                git branch: 'main', 'https://github.com/SaifKbishi/jenkines_jobs/'
                sh 'ls -ltr'
                echo 'Hello Jenkins! \n new line for what'
            }
        }
    }
}
