pipeline {
    agent any

    environment {
        // Define environment variables if needed
    }

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS106'
                sh 'g++ main.cpp -o output' 
            }
        }

        stage('Test') {
            steps {
                    // Test stage commands
                    sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure{
          error 'Pipeline failed'
        }
    }
}
