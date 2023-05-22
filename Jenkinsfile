pipeline{
    agent any
    environment {
        PATH = "/usr/bin/:$PATH"
    }
    stages {
        stage("Git checkout"){
            steps{
                git 'https://github.com/devopsfaisal/hello-world.git'
                // git branch: 'practice', url: 'https://github.com/devopsfaisal/hello-world.git'
            }
        }
        stage("Maven Build"){
            steps{
                sh 'mvn clean install'
            }
        }
    }
}
