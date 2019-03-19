pipeline {
    agent {
        label 'docker' 
    }
    stages {
        stage('Build') {
            agent {
                docker {
                  // Set both label and image
                  label 'docker'
                  image 'python'
               }
            }
            steps {
                // Download the code
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
