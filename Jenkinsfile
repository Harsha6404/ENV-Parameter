pipeline {
    agent any
    
 stages {

        stage('checkout') {
            steps {
                git 'https://github.com/Harsha6404/dockerproject.git'
            }
        }

        stage('build') {
            steps {
                sh 'docker build -t $image .'
            }
        }

        stage('tag') {
            steps {
                sh 'docker tag $image $imgtag'
            }
        }
       stage('push') {
            steps {
                sh 'docker login -u hzrshz -p $password'
                sh 'docker push $imgtag'
            }
        }
    }
    
}
