pipeline {
    agent any
    environment {
        GIT_REPO_URL = 'https://github.com/MDJ-GitHub/java-hello-world-with-maven.git/'
    }
    stages {
        stage('Checkout') {
            steps {
                // Fetch the source code from the GitHub repository
                git url: "${GIT_REPO_URL}", branch: 'main'
            }
        }
        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }
        stage('Package') {
            steps {
                // Package the application (jar, war, etc.)
                sh 'mvn package'
            }
        }
    }
    post {
        success {
            echo 'Build and packaging successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
