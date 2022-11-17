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
}
