pipeline {
    agent any
    
        
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'go version'
                sh(script: "go run main.go")
                sh(script: "go build")
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh(script: "go test")
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}