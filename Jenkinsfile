pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/sirMoksh/ABC-Technologies.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
