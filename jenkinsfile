pipeline {
    agent any
    
    stages {
        stage('Fetching code from git') {
            steps {
                git branch: 'main', url: 'https://github.com/Bharath0128/jenkins-test.git'
            }
        }
        
        stage('Installing apache') {
            steps {
                sh 'sudo yum install httpd -y'
            }
        }
        
        stage('Deploying website') {
            steps{
                sh 'sudo cp -R * /var/www/html/'
            }
        }
    }
}
