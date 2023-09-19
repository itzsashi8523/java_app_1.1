pipeline {
    agent any

    stages {
        stage('Start Printing') {
            steps {
                echo 'Starting the printing job...'
                sleep 10
            }
        }

        stage('Printing Job') {
            steps {
                // Add your printing commands or scripts here
                // For example, you can use shell commands to simulate the printing process
                sh 'echo "Printing in progress..."'
                sleep 10
            }
        }

        stage('Job Completed') {
            steps {
                echo 'Printing job completed!'
                sleep 20
            }
        }

        stage('Cleanup') {
            steps {
                // Remove the workspace directory
                deleteDir()
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
