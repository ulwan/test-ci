pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout SCM') {
            steps {
                echo '> Checking out the source control ...'
                checkout scm
            }
        }
        // stage('Docker Up') {
        //     steps {
        //         echo '> Building the docker containers ...'
        //         sh 'make -sC docker/ci/ build'
        //     }
        // }
        // stage('Composer Install') {
        //     steps {
        //         echo '> Building the application within the container ...'
        //         sh 'make -sC docker/ci/ composer'
        //     }
        // }
        // stage('Test') {
        //     steps {
        //         echo '> Running the application tests ...'
        //         sh 'make -sC docker/ci/ test'
        //     }
        // }
        // stage('Cleanup') {
        //     steps {
        //         echo '> Cleaning the docker artifacts ...'
        //         sh 'make -sC docker/ci/ clean'
        //     }
        // }
        stage('Docker Image Build') {
            steps {
                echo '> docker build -t hello:latest .'
            }
        }
        stage('Docker Image Push') {
            steps {
                echo '> Pushing the docker image ...'
            }
        }
        stage('Deploy') {
            steps {
                echo '> Deploying the application to staging ...'
            }
        }
    }
}