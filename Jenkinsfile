pipeline{
    agent any

    tools {
         maven 'Maven3'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/AbdulShukur007/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            steps{
               sh 'mvn package'
            }
        }
    }
}
