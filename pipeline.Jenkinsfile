#!groovy
node {
    checkout scm

	withEnv(["JAVA_HOME=${ tool 'jdk8' }", "PATH+MAVEN=${tool 'Maven 3.3.9'}/bin:${env.JAVA_HOME}/bin"]) {    

		stage("Build") {
			sh 'mvn clean install'
		}
	}
}