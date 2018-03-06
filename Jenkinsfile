pipeline {
  agent any
  stages {
    stage('build1') {
      parallel {
        stage('build1') {
          steps {
            echo 'hello'
            readFile 'index.html'
          }
        }
        stage('build2') {
          steps {
            echo 'build 2 parallel'
          }
        }
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            readFile 'test.html'
          }
        }
        stage('test read') {
          steps {
            fileExists 'test.html'
          }
        }
        stage('verify') {
          steps {
            fileExists 'web.txt'
          }
        }
      }
    }
    stage('done') {
      steps {
        writeFile(file: 'deploy.html', text: 'deployment done')
      }
    }
  }
}