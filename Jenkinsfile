pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/buyamm/jenkins-test.git'
            }
        }

        stage('Build'){
            steps{
                sh 'mvn clean install'
            }
        }

        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }

        stage('Deploy'){
            steps{
                echo 'Deployed! - TruongCongLy'
            }
        }
    }

    post{
        success{
            echo 'Build and Deploy succeeded - TruongCongLy'
        }

        failure{
            echo 'Build or Deploy failed! - TruongCongLy'
        }
    }

}