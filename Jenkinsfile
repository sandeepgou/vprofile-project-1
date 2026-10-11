pipeline {
    agent any
    tools {
        maven "maven3.9"
        jdk "Jdk21"
    }
    
    environment {
        SNAP_REPO = 'vpr-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'admin123'
		RELEASE_REPO = 'vprofile-release'
		CENTRAL_REPO = 'maven-central-pro'
		NEXUSIP = '172.31.43.144'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'vpro-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
