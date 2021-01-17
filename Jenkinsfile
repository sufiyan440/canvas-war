pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('package') {
            steps {
                sh "mvn package"
        stage('deploy Applicaton') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '249fb7a7-cd66-4f12-8823-c5ff9f209a94', path: '', url: 'http://13.234.29.89:8080/')], contextPath: 'first pipeline pro', war: '**/*.war'
            }
        }                
            }
        }
    }
}
