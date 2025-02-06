pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Pmthk1/66022635-Nextjs.git'
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
                sh 'docker run -d -p 20000:20000 nextjs-app'
            }
        }
    }
}
