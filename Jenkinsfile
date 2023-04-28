def gv
pipeline{
    agent any
    parameters{
        choice(name:'VERSION',choices:['1.1.0','1.2.0','1.3.0'],description:'')
    }
    // tools{
    //     maven 'Maven'
    //  }
    // environment
    // {
    //     NEW_VERSION='1.3.0'
    //     SERVER_CREDENTIALS=credentials('dockerhub-jenkins')
    // }
    stages{
        stage('init'){
            steps{
                script{
                    gv=load "script.groovy"
                }
            }
        }
        stage('build'){
            steps{
                 script{
                     gv.buildApp()
                 }
                echo "building the version ...... "
                // ${SERVER_CREDENTIALS}"
            } 
        }
        stage('test'){
            steps{
                echo 'testing the application'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploying the applicatin for the demo '
                // withCredentials([usernamePassword(credentials:'dockerhub-jenkins',usernameVariable:USER,passwordVariable:PWD) ]){  
                //     sh "some script   ${USER} ${PWD}"
                // } 
            }
        }
    }
}