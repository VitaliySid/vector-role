pipeline {
    stages {
        stage('Get role') {
            steps {
                dir('vector-role') {
                    git branch: 'main', credentialsId: 'git', url: 'git@github.com:VitaliySid/vector-role.git'
                }
            }
        }
        stage('Install molecule') {
            steps {
                sh 'pip3 install molecule==3.4.0 molecule-docker'
                sh 'pip3 install --upgrade requests==2.26.0'
            }
        }
        stage('Test role') {
            steps {
                dir('vector-role') {
                    sh 'molecule test'
                }
            }
        }
    }
}