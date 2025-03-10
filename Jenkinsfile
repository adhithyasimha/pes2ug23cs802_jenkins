pipeline {
    agent any
    
    environment {
        SRN = "pes2ug23cs802" 
    }
    
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "Building ${SRN}-1"
                    cd main
                    g++ -o ${SRN}_1 hello.cpp
                '''
            }
        }
        
        stage('Test') {
            steps {
                sh '''
                    echo "Testing by running the executable"
                    
                    ./${SRN}_1
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying application..."
                    mkdir -p deploy
                    cp main/${SRN}_1 deploy/
                    echo "Application deployed to deploy directory"
                '''
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline completed successfully'
        }
    }
}