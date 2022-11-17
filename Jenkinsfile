node('built-in') 
{
    stage('ContinuesDownload') 
    {
	  git 'https://github.com/intelliqittrainings/maven.git'
    }
    stage('ContinuesBuild')
    {
          sh 'mvn package'
    }
    stage('ContinuesDeployment')
    {
	  deploy adapters: [tomcat9(credentialsId: '331b3564-a6bb-4310-ab0a-c8eea59cf65b', path: '', url: 'http://172.31.27.178:8080')], contextPath: 'testapp', war: '**/*.war'
    }
    stage('ContinuesTesting') 
    {
          git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
          sh 'java -jar /root/.jenkins/workspace/sp/testing.jar'
    }
}
