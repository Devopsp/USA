#!/usr/bin/env groovy
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/Devopsp/USA/'],
    pipelineTriggers([
        upstream(
      threshold: 'SUCCESS',
      upstreamProjects: '../jobA/master'
    )
        githubPush()])
])

pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'pwd' 
            }
        }
        stage('Test'){
            steps {
                sh 'java -version'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
                sh 'pwd'
            }
        }
    }
}
