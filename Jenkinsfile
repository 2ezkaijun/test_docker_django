pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh 'scp -p 17593 -r . ubuntu@2.tcp.ngrok.io:/home/ubuntu/test/'
            }
        }
    }
}