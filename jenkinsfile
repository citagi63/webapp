pipeline {

    agent any
 
    stages {

        stage('Checkout') {

            steps {

                echo 'Checking out source code...'

                checkout scm

            }

        }
 
        stage('Clean and Build') {

            steps {

                echo 'Running Maven clean and build...'

                sh 'mvn clean install -DskipTests'

            }

        }

    }
 
    post {

        success {

            echo '✅ Build completed successfully!'

        }

        failure {

            echo '❌ Build failed!'

        }

    }

}

 
