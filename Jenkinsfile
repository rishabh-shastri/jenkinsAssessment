pipeline {
    agent any
     tools {
        jdk 'Java_8'
        maven 'Maven 3.6.3'
    }
    stages {
        stage('build') {
            steps {
                echo 'Building the source'
                sh 'mvn clean compile'
            }
        }
        stage('test') {
            steps {
                echo 'Testing source'
                sh 'mvn test'
            }
        }
		
    }
}
