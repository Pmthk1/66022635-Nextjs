pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Pmthk1/66022635-Nextjs/tree/v1.0.0'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Docker Build & Run') {
            steps {
                sh 'docker build -t nextjs-app .'
                sh 'docker run -d -p 3000:3000 nextjs-app'
            }
        }
    }
}
