pipeline {
    agent none
    stages {
        stage("maven install") {
            agent {
                docker {
                    image 'maven:3.5.0'
                    args '-e MAVEN_OPTS="-Xmx1024m -Xms512m"'
                }
            }
            steps {
                sh 'mvn clean install -X'
            }
        }
    }
}
