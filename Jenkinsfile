pipeline {
    agent any
tools {
  terraform 'Terraform v1.3.6'
}
    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/guruji-sende/iac-demo.git'
            }
        }
        stage('Terraform Init') {
            steps {
               sh 'terraform init'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'terraform apply -auto -approval'
            }
        }
    }
}
