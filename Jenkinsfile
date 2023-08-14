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
    
    stage("deploying the built artifact to Tomcat server")
    {
        sshagent(['8a429397-7398-4e6f-8f73-2530032fa245']) {
        sh "scp -o StrictHostKeyChecking=no target/demo.war ubuntu@54.235.230.98:/opt/apache-tomcat-9.0.78/webapps"

        }
    }
    
}
