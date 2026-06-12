pipeline {
    agent any 

    stages {
        stage('Build/Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running automated test suites...'
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'The build and test passed successfully!'
        }
        failure {
            echo 'Something went wrong.'
        }
    }
}
