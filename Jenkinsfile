node {
    stage('Download code from git ') {
    git branch: 'test', url: 'https://github.com/Ashwini0524/Devops-Project.git'
     }
    stage('Convert the code to artifacts') {
    sh 'mvn package'
     }
    stage('Deploy into container') {
    deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'test-server', path: '', url: 'http://172.31.28.199:8080')], contextPath: '/dev-app-script', war: '**/*.war'
}
}
