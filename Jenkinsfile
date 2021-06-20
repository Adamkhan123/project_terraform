pipeline {
    agent any
    tools {
  terraform 'terraform'
}
stages{
    stage('git checkout'){
        steps{
        git branch: 'main', credentialsId: 'gitaccess', url: 'https://github.com/adamkhan-sketch/project_terraform.git'
        }
    }
    stage('terraform initializing'){
        steps{
        sh 'terraform init'    
        }
    }
    stage('terraform showing plan'){
        steps{
        sh 'terraform plan'   
        }
    }
    stage('terraform resource provisioning'){
        steps{
        sh 'terraform apply --auto-approve'    
        }
    }
}
}
