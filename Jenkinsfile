pipeline {
    agent any

    tools {
        maven 'localMAVEN'
    }

    stages{
        stage('Build'){
            steps {
                bat 'cd C:\Program Files (x86)\Jenkins\workspace\maven-project'
                bat 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
