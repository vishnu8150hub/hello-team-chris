pipeline {
    agent { label 'docker-agent' }

    stages {

        stage('Check Node') {
            steps {
                sh 'hostname'
                sh 'whoami'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t hello-team-chris .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f hello-team-chris || true'
                sh 'docker run -d -p 5000:5000 --name hello-team-chris hello-team-chris'
            }
        }
    }
}
