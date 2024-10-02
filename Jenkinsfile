pipeline
{
	agent any
	stages
	{
		stage('scm checkout')
		{
			steps{ git 'https://github.com/shubhu34/rps-ant-sample.git' }
		}

		stage('ant build')
		{
			steps{withAnt(installation: 'ANT_HOME', jdk: 'JDK_HOME') {
    			sh 'ant -f build.xml -v'
			}}
		}
	}
}