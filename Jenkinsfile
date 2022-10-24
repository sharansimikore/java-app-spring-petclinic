
pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sharansimikore/java-app-spring-petclinic.git']]])
                echo 'Git CLoned successfully'
            }
        }
        
        
        stage('Build') {
            steps {
                sh './mvnw package'
                echo 'Build successfully'
            }
        }
   
    
    }
}
