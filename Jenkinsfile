pipeline {
    agent any

    // ----- PARAMETERS -----
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run Test stage?')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Completed'
        }
    }
}
