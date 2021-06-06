node {
    stage ('git simple-java-project') {
        //git clone
        git 'https://github.com/Srinath246/simple-java-project.git'
    }
    stage ('package the spring') {
        //maven package 
        sh 'mvn package'
    }
    stage('SonarQube analysis') {
    // performing sonarqube analysis with "withSonarQubeENV(<Name of Server configured in Jenkins>)"
    withSonarQubeEnv('mytest') {
      // requires SonarQube Scanner for Maven 3.2+
      sh 'mvn package'
    }
  }

}
