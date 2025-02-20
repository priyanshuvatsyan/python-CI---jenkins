pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: '3957e43f-320b-44d0-ae1b-ae2db585564b', url: 'https://github.com/priyanshuvatsyan/hello-world', branch: 'master'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                python3 -m venv venv
                . venv/bin/activate

                python3 -m pip install --upgrade pip

                if [ -f requitements.txt ]; then
                    python3 -m pip install -r requitements.txt
                else
                    echo "Error: requitements.txt not found!"
                    exit 1
                fi
                '''
            }
        }

        stage('Run Tests') {
    steps {
        sh '''
        . venv/bin/activate
        pytest tests/
        '''
    }
}


        stage('Deploy') {
            steps {
                echo 'Deployment step (To be implemented)'
            }
        }
    }
}
