pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                checkout scm
            }
        }
        
        stage('Run Script') {
            steps {
                echo 'Running the Python script...'
                sh 'python3 script.py'
            }
        }
        
        stage('Clean Up Workspace') {
            steps {
                echo 'Cleaning up workspace...'
                cleanWs()
            }
        }
    }
    
    post {
        success {
            echo  'Pipeline executed successfully!'
        }
        failure {
            echo  'Pipeline execution failed.'
        }
    }
}

