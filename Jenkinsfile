pipeline {
    agent node {
        label 'Agent-1 '
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
    }
}
