pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o pes2ug22cs367-1 main/hello.cpp'  /* Replace with your actual file */
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh 'chmod +x pes2ug22cs367-1'  // Ensure execute permissions
                    sh './pes2ug22cs367-1'  // Execute compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs for errors.'
        }
    }
}
