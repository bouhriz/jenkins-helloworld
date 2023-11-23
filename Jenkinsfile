pipeline {
    agent any 
    stages {
        stage('clone') {
            steps {
                bat 'del /q /f /s *'
                bat 'for /d %%i in (*) do @rmdir /s /q "%%i"'
                bat 'git clone https://github.com/bouhriz/jenkins-helloworld.git'
            }
        }
        stage('build') {
            steps {
                bat 'cd jenkins-helloworld && javac Main.java'
            }
        }
        stage('run') {
            steps {
                bat 'cd jenkins-helloworld && java Main'
            }
        }
    }
}
