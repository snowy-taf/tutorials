pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/eugenp/tutorials.git'
            }
        }
        stage('Navigate to tests') {
            steps {
                dir('python-modules/pytest-intro') {
                    sh 'pip install -r requirements.txt || true'
                    sh 'pytest'
                }
            }
        }
    }
}

git add Jenkinsfile
git commit -m "Добавил Jenkinsfile"
git push origin main
