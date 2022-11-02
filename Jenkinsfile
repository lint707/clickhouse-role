pipeline {
    agent any
    stages {
        stage('Git') {
            steps{
                git branch: 'main', credentialsId: 'c0005444-4342-4a55-a707-361951461222', url: 'git@github.com:lint707/clickhouse-role.git'
            }
        }
        stage('Download molecule'){
            steps{
                sh 'pip3 install molecule molecule_docker'
            }
        }
        stage('test'){
            steps{
                sh 'ls -lha'
            }
        }
        stage('Run molecule'){
            steps{
                sh 'molecule test'
            }
        }
    }
}
