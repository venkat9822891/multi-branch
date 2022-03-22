node() 
{
    stage('Continuous Download') 
	{
    git 
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment')
	{
	deploy adapters: [tomcat8(credentialsId: '68659247-e3c3-4313-99cc-37e94f5bf716', path: '', url: 'http://172.31.12.12:8080')], contextPath: '/devapp', war: '**/*.war'
	}
}
