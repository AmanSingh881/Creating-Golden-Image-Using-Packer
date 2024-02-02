pipeline {
    agent any

    stages {
        
        // Clone the GitHub repository
        stage('Git Checkout') {
            steps {
                git branch: 'main',  url: 'https://github.com/AmanSingh881/Creating-Golden-Image-Using-Packer.git'
                sh "ls"
            }
        }
        
        stage('packer image build') {
            steps {
                sh "packer init project.pkr.hcl"
                sh "packer build project.pkr.hcl"
            }
        }
    }
}
