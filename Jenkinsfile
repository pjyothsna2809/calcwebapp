node{
    stage('SCM Checkout'){
        git 'https://github.com/pjyothsna2809/calcwebapp.git'
    }
    stage('Compile Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy to Tomcat'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
