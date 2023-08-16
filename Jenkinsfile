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
                    sh 'sudo docker build -t nginx .'
            }
        }
       
        
       
    }
}
