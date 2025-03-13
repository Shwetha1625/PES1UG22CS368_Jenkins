pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec main/hello.cpp'  // Compile the C++ program
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello_exec'  // Run the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Step (Placeholder)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed! Check the logs for errors.'
        }
    }
}
