pipeline {
    agent { label 'linux' }
    tools {
      maven 'Maven-3.8.4'
    }
    stages {
        stage('Build') {
            steps {
                    sh 'mvn --version'
                    sh 'git --version'
                    sh 'sudo docker build -t nginx-docker .'
            }
        }
        stage('Run') {
            steps {
                    
                    sh 'sudo docker run -d --name nginx-docker -p 8080:80 nginx-docker'
            }
        }
        stage('Curl') {
            steps {
                    
                    sh 'curl http://localhost:8080'
            }
        }
              
    }
}
