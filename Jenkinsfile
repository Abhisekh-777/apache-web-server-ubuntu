pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Code checked out successfully"
                sh 'ls -l'
            }
        }

        stage('Install Apache') {
            steps {
                sh '''
                sudo apt update
                sudo apt install -y apache2
                '''
            }
        }

        stage('Start Apache') {
            steps {
                sh '''
                sudo systemctl start apache2
                sudo systemctl status apache2
                '''
            }
        }
    }
}
