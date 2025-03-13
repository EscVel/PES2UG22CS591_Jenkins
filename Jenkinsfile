pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS591-1 new.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    shSDDGS './PES2UG22CS591-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment steps if required
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
