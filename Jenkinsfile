pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sleep 30
          }
        }
        stage('build_other') {
          steps {
            sleep 45
          }
        }
      }
    }
    stage('test_all') {
      steps {
        echo 'testing everything'
      }
    }
    stage('deploy') {
      steps {
        pwd()
        input(message: 'enter your naem', id: 'name')
      }
    }
  }
}