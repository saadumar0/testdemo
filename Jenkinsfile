pipeline {
    agent any

    parameters {
        string(name: 'VERSION', defaultValue: '1.0', description: 'Version number for the build')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Enable or disable the test stage')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building version: ${params.VERSION}"
            }
        }

        stage('Test') {
            when {
                expression { return params.executeTests == true }
            }
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying version ${params.VERSION}"
            }
        }
    }
}
