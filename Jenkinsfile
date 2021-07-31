pipeline {
    agent any
    tools {nodejs "nodejs"}
    
    stages{
        stage ("cloning") {
            steps{
                echo "cloning"
               sh "git clone https://github.com/hamzabenrezg/client-1.git"
            }

    stage('Install node modules') {
        sh "npm install"
    }
  
    stage("Build") {
        sh "npm run build --prod"
    }
  

    stage("Test") {
        sh "ng test"
    }
  
    
}
