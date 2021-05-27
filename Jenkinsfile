node
{
    
    def mavenHome = tool name : "maven3.6.2"
    stage('checkOutCode')
    {
        git branch: 'development', credentialsId: 'c78c25ec-4df4-4d79-b2f1-fd3030a0367c', url: 'https://github.com/fiaz3186/maven-web-application.git'
        
    }
    
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    
    /*
    stage('ExecuteSonarQubeReport')
    {
        sh "${mavenHome}/bin/mvn sonar:sonar"
    } 
    stage('UploadArtifacttoNexus')
    {
        sh "${mavenHome}/bin/mvn deploy"
    }
    stage('DeployApplicationInTomcat')
    {
        sshagent(['ab2c6816-cf37-4d00-8aa9-788187d918b6'])
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.90.252.78:/usr/share/tomcat/webapps/"
        }
    

    }
    */
}
    
