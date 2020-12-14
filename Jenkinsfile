pipeline{
agent any
tools {
        maven 'MAVEN_HOME' 
    }
stages{

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