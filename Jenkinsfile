pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the C++ source code...'
                sh 'g++ -o PES1UG22CS397-1 pes1ug22cs397.cpp' // Compile the C++ file
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled application...'
                sh './PES1UG22CS397-1' // Run the compiled program
            }
        }

        stage('Deploy') {
            steps 
                echo 'Deploying application...'
                // Add actual deployment commands here if needed
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs.'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
