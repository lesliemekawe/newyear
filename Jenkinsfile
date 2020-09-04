pipeline {
    agent any
    tools {
        maven 'M2_HOME'
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
