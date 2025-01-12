#pipeline
pipeline { 
    agent any
    stages{
        stage('Code'){
            steps{
                git url: 'https://github.com/pravinmistry33/JenkinsTest.git', branch: 'master'
            }
        }
        
        stage('Build'){
            steps{
                sh 'docker build . -t my-apache-image:latest'
            }
        }
        stage('Test'){
            steps{
                echo "Testing"
            }
        }
        stage('Deploy'){
            steps{
                sh "docker run -dp 127.0.0.1:96:80 my-apache-image:latest"
            }
        }
    }
}
