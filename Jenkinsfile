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
stage('ExecuteSonarqubeReport')
{
sh "${mavenHome}/bin/mvn sonar:sonar"

}
stage('uploadartifactintoNexus')
{
sh "${mavenHome}/bin/mvn deploy"

}



}
