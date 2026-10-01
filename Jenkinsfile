pipeline{
    agent any

    environment {
        ARM_CLIENT_ID = credentials('ARM_CLIENT_ID')
        ARM_CLIENT_SECRET = credentials('ARM_CLIENT_SECRET')
        ARM_TENET_ID = credentials('ARM_TENET_ID')
        ARM_SUBSCRIPTION_ID = credentials('ARM_SUBSCRIPTION_ID')
    }

    stages{
        stage('Terraform init') {
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform Validate') {
            steps{
                sh 'terraform validate'
            }
        }
        stage('Terraform Plan') {
            steps{
                sh 'terraform plan'
            }
        }
    }
}