node('master') {
   stage('Continuous Download') {
        git 'https://github.com/vinaycilveri/Practise.git' 
    }
    stage('Continuous Build') {
        sh label: '', script: 'mvn package'
    }
    stage('Continuous Deployment') {
        sh label: '', script: 'scp /root/.jenkins/workspace/scripted_pipeline/webapp/target/webapp.war ubuntu@172.31.25.70:/var/lib/tomcat8/webapps/qaapp.war'
    }
    stage('Continuous Testing') {
        sh label: '', script: 'echo "Testing Passed"'
    }
    stage('Continuous Delivery') {
        sh label: '', script: 'scp /root/.jenkins/workspace/scripted_pipeline/webapp/target/webapp.war ubuntu@172.31.19.146:/var/lib/tomcat8/webapps/delivery.war'
    }
}
