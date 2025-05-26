node{
    stage('code checkout'){
        git 'https://github.com/gchakra9/addressbook.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    
    stage('deploy to tomcat'){
    deploy adapters: [tomcat9(credentialsId: 'tomcat-creds', path: '', url: 'http://52.90.154.146:8080/')], contextPath: 'addressbook', war: '**/*.war'    
    }
}
