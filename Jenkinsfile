pipeline{

    agent any

    tools{
       nodejs'nodejs' 
    }
    

    stages{
        stage('build-the-app'){
            steps{
                echo '>>> Build Step'
                sh 'npm install'
            }
        }
        stage('test-the-app'){
            steps{
                echo '>>> Test Step'
                sh 'npm test'
            }
        }
        stage('package-the-app'){
            steps{
                echo '>>> Package Step'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'Tata...'
        }
        
    }
    
}
