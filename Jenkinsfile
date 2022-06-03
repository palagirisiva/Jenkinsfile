pipeline {
    agent any
    
    stages {
        stage ('SCM chekout') {
            steps {
                git 'https://github.com/Akshay369vm/java-tomcat-maven-example.git'
            }
        }
        stage ('build') {
            steps {
                sh "mvn package"
            }
        }
        stage('deploy'){
            steps {
                sh""" sudo cp -r /root/.jenkins/workspace/Hello_world_Pipeline_Proj/target /root/apache-tomcat-9.0.63/webapps
                sudo /root/apache-tomcat-9.0.63/bin/startup.sh
                """ 
            }
        }
        
    } 
}    
