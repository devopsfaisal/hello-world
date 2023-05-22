pipeline{
    agent any
    stages {
        stage("Git checkout"){
            steps{
                git 'https://github.com/devopsfaisal/hello-world.git'
                // git branch: 'practice', url: 'https://github.com/devopsfaisal/hello-world.git'
            }
        }
        stage("Maven Build"){
            steps{
                withMaven(maven: 'maven-3.9.2', mavenSettingsConfig: 'MAVEN_HOME') {
                    // You can specify additional Maven options if needed
                    sh 'mvn clean install package'
                }
            }
        }
    }
}
