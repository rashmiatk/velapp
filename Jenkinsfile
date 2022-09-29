pipeline{
	agent{
		label{
			label 'built-in'
			customWorkspace '/mnt/projects1'
		}
	}
		
	stages{
		stage('install httpd'){

			steps{

				sh"yum install httpd -y"
			}

		}	
		stage('start httpd'){

			steps{

				sh"service httpd start"
			}

		}	
		stage('deploy index'){

			steps{

				sh"cp -r /mnt/projects1/index.html /var/www/html"
				sh"chmod -R 777 /var/www/html"
			}

		}	
			
	}


}
