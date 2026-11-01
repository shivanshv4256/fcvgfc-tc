pipeline {
    agent any

    stages {
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
