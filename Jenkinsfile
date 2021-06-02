node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/chandu2br/DevOpsSample00.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
}
