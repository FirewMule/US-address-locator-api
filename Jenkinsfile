pipeline{
 agent any
 stages {
 	stage ('Build'){
 		steps {
 			
 				bat 'mvn clean install'
 		}
 	}
	
	stage ('Munit Test'){
 		steps {
 			
 				bat 'mvn clean test'
 		}
 	}
 	
 	stage ('Deploy'){
 		steps {
 			
 				bat 'mvn clean package deploy mvn package deploy -DmuleDeploy -Dusername=max356 -Dpassword=@@Gaga356@@ -Dworkers=1 -Dworker.type=Micro -Denvironment=Sandbox -Dmule.version=4.2.2 -Dapplication.name=address-locator-API -DmuleDeploy'
 			}
 		}
 	}
 }