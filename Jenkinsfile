pipeline {
    agent { label 'linux-agent' }
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/liomoti/devops_test.git']]])
            }
        }
        stage ("print message") {
            steps {
                sh """
                python3 main.py
                """
            }
        }
    }
}
