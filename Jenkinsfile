pipeline {
    agent any  // Use any available agent

    stages {
        stage('Preparation') {
            steps {
                echo 'Setting up environment...'
                sh 'echo "Workspace: $WORKSPACE"'
            }
        }

        stage('Build') {
            steps {
                echo 'Running build step...'
                sh '''
                    echo "Compiling source code..."
                    # Simulate build
                    sleep 2
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '''
                    echo "Running unit tests..."
                    # Simulate tests
                    sleep 1
                '''
            }
        }

        stage('Cleanup') {
            steps {
                echo 'Cleaning up...'
                sh 'rm -rf build/ || true'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
