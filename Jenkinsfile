pipeline {
    agent any
    tools {
        jdk 'Java 11'
    }
    stages {
        stage ('Build') {
            steps {
              sh 'sh build.sh'
            }
            post {
                success {
                    archiveArtifacts artifacts: '*.jar', followSymlinks: false
                    javadoc javadocDir: 'TuxServer-API/build/docs/javadoc', keepAll: true
                }
            }
        }
    }
}