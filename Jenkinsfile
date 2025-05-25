
pipeline {
    agent any
    stages {
        stage('Build') {
            agent any




            post {
                aborted {
                    sh 'echo "Build aborted"'
                }
                changed {
                    input 'message: 'Build stage detected a change. Proceed?'
                }
            }
        }
        stage('Test') {
            agent any




            post {
                fixed {
                    bat 'echo "Tests fixed and passing"'
                }
                cleanup {
                    timeout(time: '1, unit: 'MINUTES') {'
                    sh 'echo "Cleaning up after Test stage"'
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded'
            sh 'echo Success script'
        }
        failure {
            echo 'Pipeline failed'
            sh 'echo Failure script'
        }
    }
}

