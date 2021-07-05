node{
	def app
	
	stage('Clone') {
		checkout scm
	}
	
	stage('Build image') {
		app = docker.build("punch/nginx")
	}

	stage('Run image') {
		docker.image('punch/nginx').withRun('-p 80:80) { c ->
		sh 'docker ps'
		sh 'curl localhost'
	}
	}
}
