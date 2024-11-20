pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/superpraveen/react-todo-jenkinsApp.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                sudo cp -r build/* /var/www/html/
                '''
            }
        }
    }
}
