pipeline {
    agent {
           node {
        label 'AGENT-1'
        }
    }     

    stages {
        stage('Build') {
            steps {
                echo 'Building the code'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the code'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the code'
            }
        }
        post {
            always {
                echo 'I will always says Welcome to Bangalore'
            }
        }
    }
}
