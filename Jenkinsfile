pipeline {
    agent any
    stages {
        // stage('Clone') {
        //     steps {
        //         sh '''
        //             git clone https://github.com/NarayanadasuRakesh/clinic-website-template.git
        //         '''
        //     }
        // }
        stage('Checkout') {
            steps {
                sh '''
                    ls -la
                    cd clinic-website-template
                    ls -la
                '''
            }
        }
        stage('Install Dependencies') {
            steps {
                sh '''
                    echo "Installing Dependencies"
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    echo "Building the Application"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    echo "Running Unit test cases"
                '''
            }
        }
        stage('Env Setup') {
            steps {
                sh '''
                    sudo rm -rf /usr/share/nginx/html/*
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    cd clinic-website-template
                    sudo cp -r . /usr/share/nginx/html/
                '''
            }
        }
    }
    post { 
        always { 
            echo 'This will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'This will run when pipeline is success'
        }
        failure { 
            echo 'This will run when pipeline is failure'
        }
    }
}