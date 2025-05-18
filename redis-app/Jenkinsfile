pipeline {
    agent any
    stages {
        stage('Build Redis Image') {
            steps {
                sh 'docker build -t custom-redis .'
            }
        }
        stage('Run Redis') {
            steps {
                sh 'docker run -d --name redis-server custom-redis'
            }
        }
    }
}
