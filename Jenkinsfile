pipeline {
		agent {
		node {
		label ('built-in')
		}
		}
		
		stages {
			stage ('copy-warfile') {
			steps {
			dir ('/mnt/gameoflife') {
			sh "rm -rf *"
			sh "cp /mnt/linuxm.pem /mnt/gameoflife"
			sh "scp -i linuxm.pem /mnt/apache-tomcat-9.0.65/webapps/gameoflife.war ec2-user@172.31.3.192://mnt/apache-tomcat-9.0.67/webapps"
			}
			}
			}

	}

	}
