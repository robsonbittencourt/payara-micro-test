#!groovy​

node {
    withEnv(["JAVA_HOME=${ tool 'jdk-8' }", "PATH+MAVEN=${tool 'maven'}/bin:${env.JAVA_HOME}/bin"]) {
    
    sh "mvn clean package"
}