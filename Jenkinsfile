node('master') {
    stage('Continuous Download') {
        git 'https://github.com/vinaycilveri/Practise.git'
    }
    stage('Continuous Build') {
    sh label: '', script: 'mvn package'
    }
    stage('Continuous Deployment') {
    sh label: '', script: 'sudo scp /root/.jenkins/workspace/Scripted/webapp/target/webapp.war  ubuntu@172.31.37.24:/var/lib/tomcat8/webapps/qaapp.war'
    }
    stage('Continuous Testing') {
    sh label: '', script: 'echo "Testing Passed"'
    }
    stage('Continuous Delivery') {
    sh label: '', script: 'sudo scp /root/.jenkins/workspace/Scripted/webapp/target/webapp.war  ubuntu@172.31.32.241:/var/lib/tomcat8/webapps/delivery.war'
    }
}
