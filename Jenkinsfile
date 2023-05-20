pipeline{
    
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
    
    agent any
    
    stages{

        stage('1.CloneRepo')
        {
           
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('2.Compile the code')
        {
             
            steps{
             sh 'mvn compile'
            }
        }
        stage('3.unit test')
            {
            steps{
            sh 'mvn test'
            }
            post {
                success{
                    junit 'target/surefire-reports/*.xml'
                }
            }
            }
        
 stage('4.package')
            {
            steps{
            sh 'mvn package'
            }
            }
            
            }
        
    }

    
