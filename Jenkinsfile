pipeline {
    agent any
    stages {
        stage('Clone'){
            steps {
                    sh "git clone https://github.com/Gitjeoma/QACRUD.git"
            }
        }
             stage('Build'){
            steps {
                docker{
                docker build -t ournginx .
            }
        }
       stage('test'){
            steps{
                sh "python3 m pytest --cov"  
            }
        }
         stage('deploy'){
            steps{
                sh "python app.py"
            }
        }  
    }
}
