pipeline {
    agent any
    tools {
        maven 'maven.15'
    }

    environment {
        IMAGE_NAME = 'evolve-technologies-web'
        REGISTRY = 'umamahesh571'
        DOCKER_IMAGE = "${REGISTRY}/${IMAGE_NAME}"
        REPO_URL = 'https://github.com/EvolveTechno/evolve-technologies-1'
        BRANCH = 'main'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: "${BRANCH}", url: "${REPO_URL}"
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}   
    
    
