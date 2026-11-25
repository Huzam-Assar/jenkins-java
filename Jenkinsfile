pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting code from GitHub'
                checkout scm
            }
        }

        stage('Compile Java') {
            steps {
                sh 'javac Hello.java'
            }
        }

        stage('Run Java') {
            steps {
                sh 'java Hello'
            }
        }
    }
}
