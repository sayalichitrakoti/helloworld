pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/sayalichitrakoti/helloworld.git']]])
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                // Assuming your JAR file is named "your_project_name.jar"
                bat 'java -jar target/HelloWorld-0.0.1-SNAPSHOT.jar'
            }
        }
        
    }
}
