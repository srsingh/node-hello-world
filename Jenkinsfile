pipeline {
    agent { docker { image 'node:8' } }

    tools {nodejs "node"}

    stages {

        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
        stage('Cloning Git') {
          steps {
            git 'https://github.com/sanjeevkumarrao/node-hello-world'
          }
        }

        stage('Install dependencies') {
          steps {
            sh 'npm install'
          }
        }

        stage('Test') {
          steps {
             sh 'npm test'
          }
        }
    }

}
