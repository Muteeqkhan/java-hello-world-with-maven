pipeline{
    agent any
    stages{
        stage("delete dir){
              steps{
                  deleteDir()
              }
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/sreenivas449/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            steps{
               sh 'mvn clean install'
            }
        }
    }
}
