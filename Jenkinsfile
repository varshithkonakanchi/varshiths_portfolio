pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    dockerImage = docker.build('varshithport')
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Run Docker container
                    dockerImage.run('-p 3000:80 --name varshithport')
                }
            }
        }
    }
}
