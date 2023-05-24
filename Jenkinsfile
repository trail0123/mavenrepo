pipeline{
agent {label 'dev'}
triggers {
  pollSCM '* * * * *'
}
stages{

stage('git'){
steps{
checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '3c7a00b7-995a-4249-955b-b329537d4953', url: 'https://github.com/trail0123/mavenrepo.git']])
}
}

stage('build'){
steps{
sh 'mvn package'
}
}



}
}
