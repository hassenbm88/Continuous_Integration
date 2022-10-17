pipeline{
    agent any
    tools {
        maven 'M2_HOME'
    }
    stages {
        stage('Getting project from Git') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/yassine']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/hassenbm88/CICD_Academic_Project.git'], extensions: [], userRemoteConfigs: [[credentialsId: '18558545-93a9-448f-bf74-85184c601676', url: 'https://github.com/hassenbm88/CICD_Academic_Project.git']]])
            }
        }
        
        
        stage('Cleaning the project') {
            steps{
                sh "mvn -B -DskipTests clean  " 
            }
        }
                stage('Cleaning versiont') {
            steps{
                sh "mvn --version  " 
            }
        }
        
        
        
        stage('Artifact Construction') {
            steps{
                sh "mvn -B -DskipTests package " 
            }
        }
        
         stage('Unit Tests') {
            steps{
                sh "mvn test " 
            }
        }
        
     
       
        

     
} 
}
       
