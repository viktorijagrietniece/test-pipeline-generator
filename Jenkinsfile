
pipeline {
    agent 
        any
    

    
environment {
    
    ENV = "TESTING"
    
}

 
    stages {
        
        stage('Build') {
            
            agent any
            

            
            environment {
                
            }
            

            steps {
                
                echo 'Build done'
                
            }

            
        }
        
        stage('Test') {
            
            agent any
            

            
            environment {
                
            }
            

            steps {
                
                sh 'npm test'
                
            }

            
        }
        
    }
  
    
    post {
        
        always {
            
            echo 'Pipeline done'
            
        }
        
    }
    
}
