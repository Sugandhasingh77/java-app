pipeline {
    agent any

    stages {
        stage("GIT CHECKOUT") {
            steps{
                git branch: 'main', url: 'https://github.com/Sugandhasingh77/java-app.git'
            }
        }
        stage("Unit Test") {
            steps{
                sh 'mvn test'
            }
        }
        stage("Integration Test") {
            steps{
                sh 'mvn verify -DskipUnitTests'
            }
        }
        stage("MAVEN BUILD") {
            steps{
                sh 'mvn clean install'
            }
        }
    }
}
