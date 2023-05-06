node{
    stage('Checkout'){
        checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'http://github.com/TsarAlexandr/python_test']])
    }
    stage('Docker-build'){
        sh 'sudo docker build -t prodptn .'
    }
    stage('Docker-run'){
        sh 'sudo docker run -d -p 4545:5000 prodptn'
    }
}
