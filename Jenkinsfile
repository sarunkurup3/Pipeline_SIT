pipeline{
agent any

stages{

stage('Compile Stage'){
steps{
withMaven(maven:'MAVEN_HOME'){
bat 'mvn clean compile'}
}}
stage('Build Stage'){
steps{
withMaven(maven:'MAVEN_HOME'){
bat 'mvn clean install'}
}}
stage('Test Stage'){
steps{
withMaven(maven:'MAVEN_HOME'){
bat 'mvn clean test'}
}}

}

}