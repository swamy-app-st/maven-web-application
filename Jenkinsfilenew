node
{
def mavenHome = tool name: "maven3.6.3"
stage('checkout')
{
git branch: 'dev', credentialsId: 'a4928fda-7cd4-431a-bfa6-b59228140fea', url: 'https://github.com/swamy-app-st/maven-web-application.git'
}
stage('Build')
{
sh "${mavenHome}/bin/mvn clean package"
}
  /*
stage('ExecuteSonarqubeReport')
{
sh "${mavenHome}/bin/mvn sonar:sonar"

}
stage('uploadartifactintoNexus')
{
sh "${mavenHome}/bin/mvn deploy"

}

stage('deploy aplication into tomcat server')
{
sshagent(['f0ea7212-8ebc-425e-94d5-19555de3cc6c']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ubuntu@ip-172-31-7-143:/opt/apache-tomcat-9.0.98/webapps"
}

}
stage('send email notification')
{
mail bcc: 'tech.swamy369@gmail.com', body: '', cc: 'tech.swamy369@gmail.com', from: '', replyTo: '', subject: 'Build over .....    ', to: 'tech.swamy369@gmail.com'
}
*/


}
