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
