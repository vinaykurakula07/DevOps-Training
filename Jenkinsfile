node {

stage 'checkout'
git 'https://github.com/vinaykurakula07/DevOps-Training.git'

stage 'compile'
  def mvnHome = tool name: 'maven', type: 'maven'
  sh "${mvnHome}/bin/mvn compile"

stage 'test'
sh "${mvnHome}/bin/mvn test"

stage 'package'
sh "${mvnHome}/bin/mvn package"

stage 'artifacts'
archiveArtifacts 'target/*.war'

}
