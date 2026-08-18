pipeline {
    agent any
    stages {
        stage (" Clean Up") {
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo") {
            steps {
                sh "git clone https://github.com/khalidgit123/hadoop-admin-automation.git"
            }
        }
        stage("Build") {
            steps {
                dir("hadoop-admin-automation") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test") {
            steps {
                dir("hadoop-admin-automation") {
                    sh "mvn test"
                }
            }
        }
    }
}