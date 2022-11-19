pipeline {
    agent any

    stages {
        stage('Test Sonar con Name-Discovery') {
            steps {
                withSonarQubeEnv('sonarqube') {
                    sh "echo 'Calling sonar Service in another docker container!'"
                    // Run Maven on a Unix agent to execute Sonar.
                    sh './mvnw clean verify sonar:sonar'
                }
            }
        }
    }
}
