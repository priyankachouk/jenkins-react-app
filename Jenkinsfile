pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "whoami"
                sh "sudo npm install"
                sh "npm i react-scripts"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/jenkins-react-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
