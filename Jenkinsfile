pipeline {
    agent {
        label "worker1"
    }
    stages {
        stage ("sonarqube"){
            steps {
                sh '''
                docker-compose -f sonarqube-compose.yaml down
                docker-compose -f sonarqube-compose.yaml up -d
                '''
            }
        }
    }
}