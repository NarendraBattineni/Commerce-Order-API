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
 post {
    always {
        mail bcc: '', 
             body: '''Hi, The pipeline job for Mulesoft is completed and the project was deployed to standalone server.
                      This is the conformation mail from the jenkins.
                  Regards,
                  Jenkins system''', 
              cc: '', 
              from: 'Jenkins@prolifics.com', 
              replyTo: '', 
              subject: 'Jenkins job for mulesoft demo', 
              to: 'blchanrendra@gmail.com'
}
}
