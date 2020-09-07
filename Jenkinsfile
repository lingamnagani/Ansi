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
             ansiblePlaybook becomeUser: 'Lingam', credentialsId: '84d518af-d2ff-4019-8d7d-0db03ee98dc5', disableHostKeyChecking: true, installation: 'Ansi', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
