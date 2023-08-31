pipeline {
    agent any
    stages {
        stage('Hello world'){
             steps{
                 echo 'Hello TOBI'
            }
        }
        stage('Run backend') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 rest_app.py &'
            }
        }
        stage('Run frontend') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 web_rest.py &'
            }
        }
        stage('Run backend tests') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 backend_test.py &'
            }
        }
        stage('Run frontend tests') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 frontend_test.py &'
            }
        }
        stage('Run combined tests') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 combine_testing.py &'
            }
        }
        stage('Clean environment') {
            steps {
                sh 'nohup /Users/danielgotlieb/Downloads/firstProject/venv/bin/python3 clean_environment.py &'
            }
        }
    }

}

