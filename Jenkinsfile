pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                def response =httpRequest acceptType: 'APPLICATION_JSON', contentType: 'APPLICATION_JSON',
            httpMode: 'POST', quiet: true,
            requestBody: '''{
               
                "name": "jenkinsworkspace1",
                "description": "jenkinsworkspace1",
                "type" : "Deploy",
                "owner" : "boron.element",
                "provider" :"aws",
                "cloudaccount": "aws"
            }''',
            url: 'http://10.148.27.54:8090/api/v1/workspaces?projectuuid=project-KCuCBQsi'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}