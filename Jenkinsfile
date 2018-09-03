
pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'export M2_HOME=/Users/simondavies/dev/tools/apache-maven-3.5.4'
                sh 'mvn clean package'
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
