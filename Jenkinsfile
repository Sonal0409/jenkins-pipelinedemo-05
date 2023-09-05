pipeline{
    
    tools{
       maven 'mymaven' 
    }
    
    agent any
    
    stages{
        stage('CloneRepo')
        {
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        
          stage('Review the code')
        {
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        
        stage('Compile the code')
        {
            steps{
                sh 'mvn compile'
            }
        }
        
         stage('Test the code')
        {
            steps{
                sh 'mvn test'
            }
        }
        
         stage('Package the code')
        {
            steps{
                sh 'mvn package'
            }
        }
    }
    
}

