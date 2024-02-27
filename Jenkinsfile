pipeline {  
    agent any
    stages{
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/addamstj/Jenkins-Course.git"
            }
        }
        stage("Build"){
            steps {
                dir("Jenkins-Course") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                dir("Jenkins-Course") {
                    sh "mvn test"
                }
            }
        }
    }
}