pipeline
{
agent any
tools{
maven'maven'
}
stages{
stage('Checkout')
{
	steps{
	git branch: 'master' , url: 'https://github.com/Palak-Paliwal2004/MavenApp.git'
	}
}
stage('Build')
{
	steps{
	sh 'mvn clean package'
	}
}
stage('Test')
{
	steps{
	sh 'mvn test'
	}
}
stage('Running Application')
{
	steps{
	sh 'java -jar target/MavenApp-1.0-SNAPSHOT.jar'
	}
}
}
post{
success{
	echo 'Build successful'
}
failure{
	echo 'Try again'
	}
}
}
