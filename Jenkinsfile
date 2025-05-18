pipeline {
    agent any
    stages {
        stage('Build MySQL Image') {
            steps {
                sh 'docker build -t custom-mysql .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=root custom-mysql'
            }
        }
    }
}
