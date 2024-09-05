pipeline {
    agent any

    stages {
        stage('gitjob') {
            steps {
                echo 'Cloning the code...'
                git 'https://github.com/Arunsh93/addressbook.git'
            }
        }
        stage('buildjob') {
            steps {
                echo 'Building the code...'
                sh 'mvn compile'
            }
        }
        stage('testjob') {
            steps {
                echo 'Testing the code...'
                sh 'mvn test'
            }
        }
        stage('deployjob') {
            steps {
                echo 'Deploying the code...'
                sh 'mvn install'
            }
        }
    }
}
