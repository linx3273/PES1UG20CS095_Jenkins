pipeline{
    agent any

    stages{
        stage('Clone Repository'){
            steps{
                git branch:'main',
                url : 'https://github.com/linx3273/PES1UG20CS095_Jenkins.git'
            }    
        }
        stage('Build'){
            steps{
                sh 'make'
                echo "Build Successful."
            }
        }
        stage('Test'){
            steps{
                sh './hello_exec'
                echo "Test Completed."
            }
        }
        stage('Deploy'){
            steps{
                sh 'Deployed'
            }
        }
    }
    post{
        failure{
            sh 'echo "Pipeline Failed"'
        }
    }
}
