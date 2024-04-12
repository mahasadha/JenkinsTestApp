pipeline {
    agent any

    environment {
    PATH = "C:\\WINDOWS\\SYSTEM32; C:\\Users\\vignesh\\apache-maven-3.9.6\\bin"
    JAVA_HOME='C:\\Program Files\\Java\\jdk-17'
    }

    stages {
        stage('connect') {
            steps {
                git branch:'main' , url: 'https://github.com/mahasadha/JenkinsTestApp.git'
            }
        }
        stage('build') {
            steps {
                bat 'C:\\Users\\vignesh\\apache-maven-3.9.6\\bin\\mvn clean'
                echo 'Build SUCCESSFULL'
            }
        }
        stage('test') {
            steps {
                bat 'C:\\Users\\vignesh\\apache-maven-3.9.6\\bin\\mvn test'
                echo 'Test SUCCESSFULL'
            }
        }
        stage('deploy') {
            steps {
                //deploy success
                echo 'The application is deployed SUCCESSFULLY !!'
            }
        }
    }
    
}