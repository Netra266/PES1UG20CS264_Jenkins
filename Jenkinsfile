pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ program.cpp -o task5' 
            }
        }
        stage('Test') { 
            steps {
                sh 'cat program.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                sh './task5'
                //error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
