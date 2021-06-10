pipeline{
	agent any
	tools {
		terraform 'terraform-14'
	}
	stages{
		stage('Git Checkout'){
			steps{
				git branch: 'main', credentialsId: 'de37d558-10ea-4543-977e-2c7b5b4da517', url: 'https://github.com/suresh-akidev/jenkins-demo'
			}
		}
		stage('Terraform Init'){
			steps{
				sh label: '', script: 'terraform init'
			}
		}
		stage('Terraform plan'){
			steps{
				sh label: '', script: 'terraform plan'
			}
		}
		stage('Terraform apply'){
			steps{
				sh label: '', script: 'terraform apply --auto-approve'
			}
		}
	}
}