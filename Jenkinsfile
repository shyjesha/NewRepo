node{
   stage('SCM Checkout'){
   git 'https://github.com/shyjesha/NewRepo.git'
   }
   stage('Build'){
   sh 'mvn clean package'
   }
   stage('deploying to tomcat'){
   sshagent(['tomcat8']) {
   sh 'scp -o StrictHostKeyChecking=no target/*.jar ubuntu@18.220.113.12:/opt/tomcat8/webapps/'
}
   }
}
