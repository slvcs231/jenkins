pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        course = 'Jenkins'
    }
    options {
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }

     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the code'
                script {
                    sh """
                        echo "Building"
                        echo $course
                        sleep 10
                        env
                    """
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing the code"
                        echo $course
                    """
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the code'
            }
        }
    }

    post {
        always {
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
        aborted {
            echo 'pipeline is aborted'
        }
    }
}