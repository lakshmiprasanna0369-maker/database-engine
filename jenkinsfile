pipeline{
    agent any 
    
    stages {
        stage ('checkout git'){
         steps{
             checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/lakshmiprasanna0369-maker/database-engine.git']])
         }   
        }
        stage ('validate')
        {
            steps{sh 'mvn validate'}
        }
        stage ('compile')
        {
            steps{sh 'mvn compile'}
        }
        stage ('test')
        {
            steps{sh 'mvn test'}
        }
        stage ('package')
        {
            steps{sh 'mvn package'}
        }
            }
        }
