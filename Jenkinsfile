pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o program_exec program.cpp'
                echo 'build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './program_exec'
                echo 'test stage successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
   }
    post {        
        failure {
            echo 'Pipeline failed.'
        }
    }
}
