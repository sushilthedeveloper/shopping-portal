pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
	tools{
       nodejs 'nodejs' 
    }
  

    stages{
        stage('compile-the-app'){
            steps{
                echo 'this is the Compile job'
                sh 'npm install'
            }
        }
        stage('test-the-app'){
            steps{
                echo 'this is the Test job'
                sh 'npm test'
                sleep 9
            }
        }
        stage('package-the-app'){
            steps{
                echo 'this is the Package job'
                sh 'npm run pacakage'
                sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'THe Pipeline has successfully been completed'
        }
        
    }
    
}
