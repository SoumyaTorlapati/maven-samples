node(){
    
stage("cloning the code"){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/maven-samples.git']]])
    echo "clone"
}
stage("packaging"){
   bat '''set JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_144
mvn package'''
    echo "packaging"
}
stage("Deployment"){
    bat '''cd C:\\chaitanya\\devops\\training\\july-batch
cmd /k deploy.bat'''

    echo "Deployment"
}
    
}
