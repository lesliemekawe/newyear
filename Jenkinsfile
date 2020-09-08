pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }
    environment {
        registry = "lesliemekawe/devops-pipeline"
        registryCredential = 'DockerRegistryID'
    }
    stages {
        stage('Hello') {
            steps {
                echo 'happy new year'
            }
        }
        stage('build') {
            steps {
                echo 'hello build' 
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('deployr') {
            steps {
                script {
                    docker.build registry + ":$BUILD_NUMBER"
                }
            }
        }
    }
        
}
