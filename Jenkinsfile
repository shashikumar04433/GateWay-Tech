#!/groovy
def dockerImageRepo = 'gatewaytech/gatewaytech-ui'
def dockerImageTag
def dockerImage
def dockerRegistry = 'hub.docker.com'

pipeline
{
	agent any
	stages
	{
		stage('Cleaning the WorkSpace')
		{
			steps
			{
				deleteDir()
				echo "the build number is ${currentBuild.number}"
				echo 'Cleanup Done'
			}
		}
		
		stage('CheckOut latest Code')
		{
			steps
			{
				checkout scm
				script 
				{
					dockerImageTag="$BUILD_NUMBER"
				}
			}
		}
	}
}
