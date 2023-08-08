pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Modify the 'url' parameter to your repository URL
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/sayalichitrakoti/helloworld.git']]])
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        // Add more stages for deployment, testing, etc. as needed
    }
}
