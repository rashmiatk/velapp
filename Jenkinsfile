pipeline{
	agent{
		label{
			label 'slave'
			customWorkspace '/mnt/data'
		}
	}
		
	stages{
		stage('install httpd'){

			steps{

				sh"sudo yum install httpd -y"
			}

		}	
		stage('start httpd'){

			steps{

				sh" sudo service httpd start"
			}

		}	
		stage('deploy index'){

			steps{

				sh"sudo cp -r /mnt/data/index.html /var/www/html"
				sh"sudo chmod -R 777 /var/www/html"
			}

		}	
			
	}


}
