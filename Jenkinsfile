pipeline {
    agent any
    
    parameters {
        string(name: 'VERSION', defaultValue: '1.1.0', description: 'Build version')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests?')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building Project... Version: ${params.VERSION}"
            }
        }
        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing Project...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project...'
            }
        }
    }
}
