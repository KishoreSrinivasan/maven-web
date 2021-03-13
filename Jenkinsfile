pipeline {
    
    agent any
    
    environment {
        PATH="/opt/maven3/bin:$PATH"
    }
    
    stages {
        
        stage('git checkout') {
            steps {
                git credentialsId: 'GitHubCredentials', url: 'https://github.com/KishoreSrinivasan/maven-web.git'
            }
        }
        
        stage('maven build') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
