node
{
    def mavenHome = tool name: "mymaven"
    
    stage("checkout code from GIT")
    {
        git branch: 'main', url: 'https://github.com/maveric-coder/java_war_project.git'
    }
    
    stage("building the artifiact")
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    
    stage("deploy to tomcat server")
    {
        
    }
    
}
