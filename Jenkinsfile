pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/yourusername/hello-team-chris.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-team-chris .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 hello-team-chris'
            }
        }
    }
}
