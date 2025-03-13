pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec hello.cpp'  // Compiles hello.cpp
            }
        }

        stage('Test') {
            steps {
                sh './hello_exec'  // Executes compiled binary
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
