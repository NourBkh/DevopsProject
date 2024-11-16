pipeline {
    agent any

    parameters {
        string(name: 'NEXUS_URL', defaultValue: 'localhost:8081', description: 'Nexus URL')
        string(name: 'NEXUS_REPOSITORY', defaultValue: 'maven-releases', description: 'Nexus Repository Name')
        string(name: 'SONARQUBE_URL', defaultValue: 'http://localhost:9001', description: 'SonarQube URL')
        string(name: 'PROMETHEUS_URL', defaultValue: 'http://localhost:9090', description: 'Prometheus URL')
        string(name: 'GRAFANA_URL', defaultValue: 'http://localhost:3000', description: 'Grafana URL')
    }

    environment {
        DB_URL = 'jdbc:mysql://localhost:3307/devops'
        DB_USER = 'root'
        DB_PASSWORD = ''
        SONAR_DB_URL = 'jdbc:postgresql://sonar_db:5432/sonar'
        SONAR_DB_USER = 'sonar'
        SONAR_DB_PASSWORD = 'sonar'
        DOCKER_USERNAME = credentials('dockerhub-token')
        DOCKER_PASSWORD = credentials('dockerhub-token')
        IMAGE_NAME_BACKEND = 'nourbkh/devops-backend'
        IMAGE_TAG_BACKEND = 'nourbenkhairia-5arctic3-g4-devops'
        IMAGE_NAME_FRONTEND = 'nourbkh/devops-frontend'
        IMAGE_TAG_FRONTEND = 'nourbenkhairia-5arctic3-g4-devopsfrontend'
        SONAR_SCANNER_HOME = tool 'SonarQube Scanner'
        SONAR_PROJECT_KEY_BACKEND = 'devops-backend'
        SONAR_PROJECT_KEY_FRONTEND = 'devops-frontend'
        SONAR_TOKEN = credentials('sonarqube-token')
        NEXUS_CREDENTIALS = credentials('nexus-credentials')
        MAVEN_REPO_ID = 'nexus'
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        CHROME_BIN = '/usr/bin/google-chrome'
        NOTIFICATION_EMAIL = 'nour.benkairia@gmail.com'
    }

    tools {
        nodejs 'Node 23'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'nourbenkhairia_5Arctic3_G4',
                    url: 'https://github.com/devopsproject976/5ArcTIC_G4_devops.git',
                    credentialsId: 'devops-pipeline'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Docker Build') {
            steps {
                echo "Building Docker images..."
            }
        }

        stage('Integration Test') {
            steps {
                echo "Running integration tests..."
            }
        }
    }
}
