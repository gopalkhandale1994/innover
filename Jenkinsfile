pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/gopalkhandale1994/innover.git'
            }
        }
        stage('Deploy to Apache') {
            steps {
                sh 'sudo cp index.html /var/www/html/index.html'
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}

