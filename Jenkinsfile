node{

def mavenHome = tool name: "maven3.8.3"

stage('Checkout'){
git branch: 'development', credentialsId: 'ba5febca-5ffe-4a81-b78c-2d1bde777776', url: 'https://github.com/bhavanisankar9963/maven-web-application.git'
}
stage('build'){
sh "${mavenHome}/bin/mvn clean package"
}
    
/*
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}


stage('Upload Artifact into nexus'){
sh "${mavenHome}/bin/mvn deploy"
}

stage('Deploy application into Tomcat server'){

sshagent(['4c969c0e-7b7f-45c1-a522-247c2bd54402']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@54.252.144.99:/opt/apache-tomcat-9.0.86/webapps"
    
}
}
*/

}
