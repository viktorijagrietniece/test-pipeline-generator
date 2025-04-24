pipeline {
    agent any

    environment {
        ENV = "TESTING"
    }

    stages {
        stage('Build') {
            agent any
            steps {
                echo 'Build done'
            }
        }

        stage('Test') {
            agent any
            steps {
                bat 'npm test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline done'
        }
    }
}
