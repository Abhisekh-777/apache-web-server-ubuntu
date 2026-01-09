pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Code pulled from GitHub'
                sh 'ls -l'
            }
        }

        stage('Install Apache') {
            steps {
                sh '''
                sudo apt update
                sudo apt install -y apache2
                sudo systemctl start apache2
                sudo systemctl status apache2
                '''
            }
        }
    }
}
