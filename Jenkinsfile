pipeline {
    agent any

    stages {
        stage('Pull git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/shivanshv4256/fcvgfc-tc'
            }
        }
        stage("BUild image"){
            steps {
                sh "docker build -t myimg ."
            } 
        }
        stage("Run container"){
            steps {
                sh "docker run ---name myweb -d -p 80:80 myimg"
            } 
        }
    }
}
