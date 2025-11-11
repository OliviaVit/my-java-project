pipeline {
    agent any
    tools {
        maven 'Maven' 
    }
    stages {
        stage('Build, Test & Analyze') { 
            steps {
                withSonarQubeEnv('SonarQube') { 
                    sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=my-java-project -Dsonar.host.url=http://sonar:9000'
                }
            }
        }
    }
}
