pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/your-nestjs-repo.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm run test'
            }
        }
    }

    post {
        always {
            echo 'CI Test Pipeline completed.'
        }
    }
}
