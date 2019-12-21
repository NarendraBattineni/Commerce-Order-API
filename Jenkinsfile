pipeline{
 agent any
 tools {
       maven 'maven'
       jdk 'JAVA_HOME'
 }
 stages {
 	stage ('Build'){
 		steps {
 			     bat 'mvn clean install'
 		}
 	}
 	stage ('Deploy'){
 		steps {
        bat 'cd target & move *.jar D:/mule-server-23112019/apps'
 			    }
 		 }
 	}
}
