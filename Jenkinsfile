pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                echo 'checking'
                git url: 'https://github.com/Yosra-10/nour.git', branch: 'main'
            }
        }
        stage('build') {
            steps {
                echo 'building'
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'docker build -t test .'
            }
        }
    }
}

