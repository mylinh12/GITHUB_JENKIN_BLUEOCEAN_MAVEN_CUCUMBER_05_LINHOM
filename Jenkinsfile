pipeline {
  agent any
  stages {
    stage('GET CODE') {
      steps {
        git(url: 'https://github.com/mylinh12/GITHUB_JENKIN_BLUEOCEAN_MAVEN_CUCUMBER_05_LINHOM', branch: '01_feature_file')
      }
    }
    stage('RUN TEST') {
      parallel {
        stage('CLEAN TEST') {
          steps {
            bat 'mvn clean'
          }
        }
        stage('RUN TEST') {
          steps {
            bat 'mvn test verify'
          }
        }
      }
    }
  }
}