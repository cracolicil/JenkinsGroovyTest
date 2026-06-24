node('DOTNETCORE'){
	stage('SCM') {
		echo 'Gathering code from version control'
		git branch: '${branch}', url: 'https://github.com/cracolicil/JenkinsGroovyTest.git'
	}
    stage('Build') {
        echo 'Building....'
		withDotNet(sdk: "sdk10"){
			sh 'dotnet --version'
			sh 'dotnet build ConsolApp1'
		}
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}