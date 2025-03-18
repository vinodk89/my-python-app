pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-pat',  // Use the correct credential ID
                    url: 'https://github.com/vinodk89/my-python-app.git'
            }
        }

        stage('Run Tests'){
            steps {
                sh '$HOME/.local/bin/pytest tests/'
            }
        }
    }
}