pipeline{
 agent any
 stages {
 	stage ('Build Application'){
 		steps {
 			
 				bat 'mvn clean install'
 		}
 	}
 	
 	stage ('Test Application'){
 		steps {
 			
 				bat 'mvn clean test'
 		}
 	}

 	stage ('Deploy Application'){
 		steps {
 			
 				bat 'mvn clean package deploy mvn package deploy -DmuleDeploy -Dusername=max356 -Dpassword=@@Gaga356@@ -Dworkers=1 -Dworker.type=Micro -Denvironment=Sandbox -Dapplication.name=address-locator-API -DmuleDeploy'
 			}
 		}
 	}
 }