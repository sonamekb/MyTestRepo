pipeline {
  agent any
  stages {
    stage('build1') {
      steps {
        echo 'hello'
        readFile 'index.html'
      }
    }
    stage('test') {
      steps {
        readFile 'test.html'
      }
    }
    stage('done') {
      steps {
        writeFile(file: 'deploy.html', text: 'deployment done', encoding: 'html')
      }
    }
  }
}