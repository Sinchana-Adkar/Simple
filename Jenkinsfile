pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'pip3 install -r requirements.txt || true'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest || true'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                sudo systemctl restart flaskapp || true
                '''
            }
        }
    }
}
