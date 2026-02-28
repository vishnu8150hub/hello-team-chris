pipeline {
    agent any

    stages {

        stage('Build Image') {
            steps {
                sh 'docker build -t hello-team-chris .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f hello-team-chris || true'
                sh 'docker run -d --name hello-team-chris -p 5000:5000 hello-team-chris'
            }
        }
    }
}
