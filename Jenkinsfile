pipeline {
  agent none

  stages {
    stage('maven') {
      agent {docker "maven"}
      steps {
        sh "mvn -version"
        sh "java -version"
      }
    }
    stage('node') {
      agent {docker "node"}
      steps {
        sh "node --version"
      }
    }
    stage('golang') {
      agent {docker "golang"}
      steps {
        sh "go --version"
      }
    }
  }
}
