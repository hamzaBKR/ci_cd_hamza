pipeline {
    agent any
    tools {
        jdk 'jdk17'
        maven 'maven_3'
    }
    stage{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
                }
                                   
	       }

        stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/hamzaBKR/ci_cd_hamza.git'
                }
        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }
		}
	}


      
   
  
}
