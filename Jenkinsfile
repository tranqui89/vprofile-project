pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'wwNSyvhIn13VJep0lSlQ'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_IP = '52.184.68.10'
        NEXUS_PORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-repo'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages{
        stage('Build'){
            sh 'mv -s settings.xml -DskipTests install'
        }
    }
}
