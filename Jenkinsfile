pipeline {
    agent any

    stages {
        stage('Start Printing') {
            steps {
                echo 'Starting the printing job...'
            }
        }

        stage('Printing Job') {
            steps {
                // Add your printing commands or scripts here
                // For example, you can use shell commands to simulate the printing process
                sh 'echo "Printing in progress..."'
                sh 'sleep 5' // Simulate a 5-second printing job
            }
        }

        stage('Job Completed') {
            steps {
                echo 'Printing job completed!'
            }
        }

        stage('Cleanup') {
            steps {
                // Remove the workspace directory
                dir('workspace') {
                    deleteDir()
                }
                echo 'Workspace cleanup complete'
            }
        }
    }

    post {
        success {
            echo 'Printing job was successful!'
        }
        failure {
            echo 'Printing job failed!'
        }
    }
}
