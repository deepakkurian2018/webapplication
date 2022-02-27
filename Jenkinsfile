pipeline{
    agent any
    tools {
        jdk 'java_home'
        maven 'maven_home' 
    }
    stages{
        stage("checkout"){
            steps{
                checkout([$class: 'GitSCM',
                branches: [[name: '*/master']],
                extensions: [],
                userRemoteConfigs: [[credentialsId: 'git_cred',
                                    url: 'https://github.com/deepakkurian2018/webapplication.git']]])
            }
        }
        stage("test"){
            steps{
                echo "this is tested"
            }
        }
         stage("QA"){
            steps{
                echo "this is tested"
            }
        }
      stage("build"){
            steps{
                echo "this is tested"
                sh """
                mvn clean install
                """
            }
        }  
        stage("artifactory push"){
            steps{
                echo "this is tested"
            }
        }  
        stage("create image"){
            steps{
                echo "this is tested"
            }
        }  
        stage("deploy to k"){
            steps{
                echo "this is tested"
            }
        }  
    }
    post{
        success{
            echo "this is post"
        }
    }   
}
