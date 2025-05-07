pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the repository...'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python -m unittest discover -s .'
            }
        }
    }
}
