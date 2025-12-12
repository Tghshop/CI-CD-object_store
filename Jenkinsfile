 
pipeline {
    agent any
    stages {
        stage('Build-Application') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Publish-to-exchange') {
            steps {
                bat 'mvn clean deploy -DskipTests'
            }
        }
        stage('Build-and-Deploy') {
            steps {
                bat 'mvn clean deploy -DmuleDeploy'
            }
        }
    }
}
 
 