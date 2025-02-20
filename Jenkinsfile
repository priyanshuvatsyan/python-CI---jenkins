pipline{
    agent any
    
    stages{
        stage('clone repo'){
            step{
                            git 'https://github.com/priyanshuvatsyan/hello-world.git'
            }

        }
        stage('install dependencies'){
            step{
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run tests'){
            step{
                sh 'pytest'
            }
        }
        stage{
            step{
                echo 'Deployment step (To be implemented)'
            }
        }
    }
    
}