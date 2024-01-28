pipeline{
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
         SNAP_REPO = 'vprofile_snapshot'
         NEXUS_USER = 'admin'
         NEXUS_PASS = 'admin123'
         RELEASE_REPO = 'vprofile_release'
         CENTRAL_REPO = 'vpro_maven_central'
         NEXUSIP = '172.31.59.2'
         NEXUSPORT = '8081'
         NEXUS_GRP_REPO = 'vpro_maven_group'
         NEXUS_LOGIN = 'nexuslogin' 
         SONARSERVER = 'sonarserver'
         SONARSCANNER = 'sonarscanner'
    }

    stages {
        stage('Build') {
            steps {
               sh 'mvn clean install -U -DskipTests -Dmaven.repo.local=~/.m2/repository'
            }
       }
}
}