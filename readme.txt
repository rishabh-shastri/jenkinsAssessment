A Jenkinsfile is a text file that contains the definition of a Jenkins Pipeline and is checked into source control. 

It consists of stages defined in it.

Example : 

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
		stage('deploy') {
            steps {
                echo 'Testing source'
                sh 'mvn package'
            }
        }
    }
}

It has following stages :

1. build stage where we have run mvn clean compile command.
2. test stage where we have run mvn test command.
3. deploy stage where we have run mvn package command.

We have also defined the tools we have used : java_8 and maven 3.6.3.

This code is written in 'Groovy' language.