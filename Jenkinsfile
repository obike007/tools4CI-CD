pipeline{
    agent any
    
    stages{
        stage ('Print Envs'){
            steps{
                sh 'printenv'
            }
        }
        stage ('Git Version'){
            steps {
                sh 'sudo yum install git -y'
                sh 'git version'
            }
        }
        stage ('Get Maven'){
            steps {
                sh 'sudo yum install maven -y'
                sh 'mvn --version'
            }
        }
        stage ('Get Docker'){
            steps {
                sh 'sudo yum install docker -y'
                sh 'sudo systemctl enable docker.service'
                sh 'sudo systemctl restart docker.service'
                sh 'docker --version'
            }
        }
        stage ('Get httpd'){
            steps {
                sh 'sudo yum install httpd -y'
                sh 'sudo systemctl restart httpd'
                sh 'httpd -version'
            }
        }
        
    }
}
