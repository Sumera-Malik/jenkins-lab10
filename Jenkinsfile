pipeline {
    agent any

    // ----- PARAMETERS -----
    parameters {
        booleanParam(name: 'executeTests',
                     defaultValue: true,
                     description: 'Run Test stage?')
    }

    // ----- ENVIRONMENT VARIABLES -----
    environment {
        VERSION = '1.0.0'
    }

    stages {
        stage('Build') {
            steps {
                echo "Building... Version: ${VERSION}"
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
