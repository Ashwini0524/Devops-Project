node {
    stage('Download code from git ') {
    git branch: 'Devops-Project', url: 'https://github.com/Ashwini0524/Devops-Project.git'
     }
    stage('Convert the code to artifacts') {
    sh 'mvn package'
     }
    stage('Deploy into container') {
    deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '6a5b5396-97b1-4cc4-8391-3ff853a58a62', path: '', url: 'http://172.31.22.172:8080')], contextPath: '/dev-app-scripted', war: '**/*.war'
}
}
