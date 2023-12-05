pipeline {
  agent any
  stages {
    stage('say hello') {
      parallel {
        stage('say hello') {
          steps {
            echo 'Hello to myself'
            sleep 5
          }
        }

        stage('write a file') {
          steps {
            writeFile(file: 'filetoupload', text: 'this is the file to upload')
          }
        }

      }
    }

    stage('build freestyle job') {
      steps {
        build 'freestyleread'
      }
    }

    stage('say goodbye') {
      steps {
        echo 'goodbye'
      }
    }

  }
}