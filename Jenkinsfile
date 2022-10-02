pipeline{
	agent {
	label {
		label '172.31.33.24'
		customWorkspace '/home/ec2-user'
		}
	}
          stages {
		stage ('install-httpd') {
			steps {
				sh "sudo yum install httpd -y"
				}
			}
		stage ('service start') {
                        steps {
                                sh "sudo service httpd start"
                                }
                        }
		stage ('copy index') {
                        steps {
                                sh "sudo cp -r /home/ec2-user/index.html /var/www/html"
                                }
                        }
		}
	}
