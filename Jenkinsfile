pipeline {
    agent any
    stages {
        stage('Secure Access') {
            steps {
                withCredentials([string(credentialsId: 'mySecret', variable: 'TOKEN')]) {
                    sh '''
                        echo "Using secret safely"
                        curl -H "Authorization: Bearer $TOKEN" https://api.example.com
                    '''
                }
            }
        }
    }
}
