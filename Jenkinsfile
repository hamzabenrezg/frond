node {
    stages{
        stage ("cloning") {
            steps{
                echo "cloning"
               sh "git clone https://github.com/hamzabenrezg/client-1.git"
            }

    stage('Install node modules') {
        sh "npm install"
    }

    stage("Test") {
        sh "npm run test-headless"
    }

    stage("Build") {
        sh "npm run build --prod"
    }
    
    stage("Copy") {
        sh "cp -a /var/lib/jenkins/workspace/angular-pipeline/dist/jenkins-test/. /var/www/jenkins_test/html/"
    }
}
