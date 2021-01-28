node {
    def name ="vikas"
    def mvn_home ="tool name: 'Maven_home', type: 'maven'"
    echo " Welcome to jenkins ${name}"
    node {
        stage('SCM Checkout'){
        git credentialsId: 'Github-Credential', url: 'https://github.com/vikas99341/maven-app.git'
        }
        stage('Maven clean step'){
        sh '${mvn_home}/bin/mvn clean'
        }
        stage('Maven Compile step'){
        sh '${mvn_home}/bin/mvn compile'
        }
        stage('Maven Test step'){
        sh '${mvn_home}/bin/mvn test'
        }   
        stage('Maven Package step'){
        sh '${mvn_home}/bin/mvn package'
        }        
    }
}
