pipeline{
	 agent any
	 
		stages {
			stage ('Compile Stage') {
				steps{
					withMaven(maven : 'Maven') {
						bat "mvn clean compile"
						}
					}
				}
			stage ('Testing Stage') {
				steps {
					withMaven(maven : 'Maven') { 
						bat "mvn test"
					}
				}
			}
			
			stage ('Package Stage') {
				steps {
					withMaven(maven : 'Maven') {
						bat "mvn package "
					}
				}
			}
			
			stage ('install Stage') {
				steps {
					withMaven(maven : 'Maven') {
						bat "mvn install"
					}
				}
			}
		}
	}
