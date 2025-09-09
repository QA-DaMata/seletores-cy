pipeline {
    agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage('Setup') {
            steps {
                git branch: 'pipeline', url: 'https://github.com/QA-DaMata/seletores-cy.git'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'NO_COLOR=1 npm test'
            }
        }
    }
}
