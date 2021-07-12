pipeline{
    agent any
    stages{
        stage('Build package'){
            steps{
                sh 'mvn -f java-tomcat-sample/pom.xml clean package'
            }
            post{
                success{
                    archiveArtifacts archive: '**/*.war'
                }
            }
        }
    }
}