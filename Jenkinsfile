pipeline {

    agent any

    tools {

        maven "MAVEN"
    }

    
    stages {
        stage('Build Maven') {
            steps{
                git branch: 'main', credentialsId: 'git_ssh_jenkins', url: 'https://github.com/SB-A/jenkins-maven-git-.git'

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
    
}
