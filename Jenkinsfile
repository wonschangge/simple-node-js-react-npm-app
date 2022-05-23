pipeline {
    agent {
        docker {
            image 'node:16-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
                    sh 'npm config ls'
                    sh 'npm -v'
                    sh 'npm --registry https://registry.npm.taobao.org'
                    sh 'npm config ls'
                    sh 'npm install' 
                }
            }
        }

    }
}
