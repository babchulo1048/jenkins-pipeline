pipeline {
    agent any

    environment {
        BRANCH_NAME = 'main'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: "${BRANCH_NAME}", url: 'https://github.com/babchulo1048/jenkins-pipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

//         stage('Deploy') {
//             steps {
//                 sh 'scp target/*.jar user@your-server:/path/to/deploy/'
//                 sh 'ssh user@your-server "systemctl restart your-app"'
//             }
//         }
    }
}
