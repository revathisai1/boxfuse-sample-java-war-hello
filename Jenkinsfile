pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
                git 'https://github.com/boxfuse/boxfuse-sample-java-war-hello.git'
            }
        }
         stage('continuous build') {
            steps {
                sh 'mvn install'
            }
        }
         stage('continuous deploy') {
            steps {
                sh cp 'target/hello-1.0.war /home/revathi/Distros/apache-tomcat-9.0.62/webapps'
            }
        }
    }
}
