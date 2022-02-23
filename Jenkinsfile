pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('compilation'){
            steps{
                echo 'this is the compile job'
                sh 'npm install'
             }
        }
        stage('testing'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
            }
        }
        stage('packaging'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'pipeline created via code..by antony..'
        }
        
    }
    
}
