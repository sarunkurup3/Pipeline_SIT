pipeline{
agent any
tools {
        maven 'MAVEN_HOME' 
    }
stages{

stage('Checkout')
    {
    step{
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '69277e6d-d6c6-44c4-b736-e4eb410dc10e', url: 'https://github.com/sarunkurup3/Pipeline_SIT.git']]]) 
    	}
    }
    

stage('Compile Stage'){
steps{
bat 'mvn clean compile'
}}

stage('Build Stage'){
steps{
bat 'mvn clean install'
}}

stage('Test Stage'){
steps{
bat 'mvn clean test'
}}

}

}