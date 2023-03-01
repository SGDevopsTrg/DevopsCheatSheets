node('MAVEN-JDK8'){
  stage('version control'){
    git url: 'Fork https://github.com/wakaleo/game-of-life.git',
        branch: 'scripted',
        poll: false
  }
  stage('build the code'){
    sh 'export PATH="/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PATH" && mvn package'
  }
  stage('archive the artifacts'){
    archiveArtifacts
        artifacts:
        allowEmptyArchive: false
  }
  stage('SHow the test Results'){
    junit
        testResults: ''
        allowEmptyArchive: false
  }
}
