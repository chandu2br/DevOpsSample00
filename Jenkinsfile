node('master') 
{
    	stage('Continuous Download') 
	{
    	git 'https://github.com/chandu2br/DevOpsSample00.git'
	}
	stage('Continuous Build') 
	{
    	sh 'mvn package'
	}
	stage('Continuous Deployment') 
	{
    	sh 'scp  /root/.jenkins/workspace/MultiBranchPipeline_master@2/webapp/target/webapp.war   ubuntu@172.31.21.88:/var/lib/tomcat8/webapps/qaenv.war'
	}
	stage('Continuous Testing') 
	{
    	sh 'echo "Tesing Passed"'
	}
	stage('Continuous Delivery') 
	{
    	sh 'scp  /root/.jenkins/workspace/MultiBranchPipeline_master@2/webapp/target/webapp.war   ubuntu@172.31.22.52:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
