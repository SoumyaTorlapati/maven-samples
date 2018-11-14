node(){
    
stage("cloning the code"){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: ' https://github.com/SoumyaTorlapati/maven-samples.git']]])
    echo "clone"
}
stage("packaging"){
   bat '''set JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_191
mvn package'''
    echo "packaging"
}
stage("Deployment"){
    bat '''cd E:\\Devops Training\\Devops Practice
cmd /k deploy.bat'''

    echo "Deployment"
}
    
}
