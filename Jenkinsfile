pipeline{
    agent any

    stages{
        

        stage('Build'){
            steps{
                sh 'java --version'
                sh 'mvn --version'
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