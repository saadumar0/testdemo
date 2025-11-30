pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }

        post {
            // execute after build

        always {
            // always happen
            echo 'Post build condition running'
        }

        failure {
            // only if build has failed
            echo 'Post Action If Build Failed'
        }
        }
}
