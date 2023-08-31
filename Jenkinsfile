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
                sh 'nohup python rest_app.py &'
            }
        }
        stage('Run frontend') {
            steps {
                sh 'nohup python web_rest.py &'
            }
        }
        stage('Run backend tests') {
            steps {
                sh 'nohup python backend_testing.py &'
            }
        }
        stage('Run frontend tests') {
            steps {
                sh 'nohup python frontend_testing.py &'
            }
        }
        stage('Run combined tests') {
            steps {
                sh 'nohup python combined_testing.py &'
            }
        }
        stage('Clean environment') {
            steps {
                sh 'nohup python clean_environment.py &'
            }
        }
    }

}

