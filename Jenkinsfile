pipeline {
  agent any

  stages {
  	stage('Checkout') {
  	  steps {
  		git 'https://github.com/edureka-git/DevOpsClassCodes'
  	  }
  	}

  	stage('SampleCompile') {
  	  steps {
  		dir('') {
  		  sh '/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven-3.6.0/bin/mvn compile'
  		}
  	  }
  	}

  	stage('Demo1') {
  	  steps {
  		dir('') {
  		  sh '/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven-3.6.0/bin/mvn tes'
  		}
  	  }
  	}

  	stage('Package') {
  	  steps {
  		dir('') {
  		  sh '/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven-3.6.0/bin/mvn package'
  		}
  	  }
  	}
  	stage('Deployment') {
  	  steps {
        // Deployment
  		script {
  		  echo "deployment"
        }
  	  }
  	}
  }
}
