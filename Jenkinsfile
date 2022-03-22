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
    deploy adapters: [tomcat8(credentialsId: '2f644474-e2a3-4d08-8f26-08d0ec5dca31', path: '', url: 'http://172.31.38.214:8080')], contextPath: '/prdapp', war: '**/*.war'
	}

}
