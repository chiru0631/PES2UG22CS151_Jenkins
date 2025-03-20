pipeline {
    agent any 
    stages {
        
        stage('Build') {
            steps {
                build 'PES2UG22CS151-1'  
                sh 'g++ main.cp -o output' 
            }
        }

        stage('Test') {
            steps { 
                sh './outpt' 
            }
        }

        stage('Deploy') { 
            steps { 
                ech 'Deployed' 
            } 
        } 

    } 

    post { 
        failure { 
            error 'Pipeline failed' 
        }  
    }  
}
