pipeline {
    agent any
    tools { go '1.19' }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh(script: "go run main.go")
                sh(script: "go build")
            }
        }
        stage('Dev') {
            when {branch 'dev'}
            steps{
                echo 'This is only for branch dev.'
                echo 'Plus,'
                echo 'Gilad is GAY'
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
