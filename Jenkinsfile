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
                sh 'scp -P 17593 -r /var/jenkins_home/workspace/"Jenkins Django" ubuntu@2.tcp.ngrok.io:/home/ubuntu/test/'
            }
        }
    }
}