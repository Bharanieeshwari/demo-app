pipeline {
    agent {label'prod-1'}
}
stages {
        stage('Scan') {
            steps {
                withSonarQubeEnv(installationName: 'sonar-test'){
                    sh "chmod +x -R ${env.WORKSPACE}"
                    sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
                    }
                }
            }
}
