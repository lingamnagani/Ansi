Pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git 'https://github.com/lingamnagani/Ansi.git'
            }
        }
        stage('Execute Ansible'){
            steps{
             ansiblePlaybook credentialsId: 'privatekey', disableHostKeyChecking: true, installation: 'Ansi', inventory: 'dev.inv', playbook: 'apache.yml'  
            }
        }
    }
}
