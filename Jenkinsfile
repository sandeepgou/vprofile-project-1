pipeline {
    agent any
    tools {
        maven "maven3.9"
        jdk "jdk21"
    }
    
    environment {
        SNAP_REPO = 'vpr-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Sandy@4317'
		RELEASE_REPO = 'vprofile-release'
		CENTRAL_REPO = 'maven-central-pro'
		NEXUSIP = '172.31.35.207'
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
