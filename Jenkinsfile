node('master') 
{
    stage('Continuous Download') 
	{
    git 
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
}
