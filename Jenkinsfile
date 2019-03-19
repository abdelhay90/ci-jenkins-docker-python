pipeline {
    // agent { docker { image 'python' } }
    agent any
    stages {
        stage('Build') {
            steps {
                // Download the code
                sh 'docker pull python'
                checkout scm
            }
        }
        stage('Test') {
            steps {
                // Run the tests
                sh 'python test_calculator.py'
            }
        }
    }
}
