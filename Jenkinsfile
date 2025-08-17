pipeline {
    agent any
  
    tools {
      maven 'Maven 3.9.6'
    }

    stages {
        stage('build') {
            steps {
                echo 'Compiling sysfoo aap'
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                echo 'Running Application unit test cases'
                sh 'mvn clean test'
            }
        }
        stage('package') {
            steps {
                echo 'packaging the app...'
                sh 'mvn package -DskipTests'
            }
        }
    }

    post{
      always{
        echo 'This pipeline completed'
      }
    }
}
