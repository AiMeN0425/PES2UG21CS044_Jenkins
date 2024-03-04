// pipeline {
//   agent any
//   stages {
//     stage('Build') {
//       steps {
//         sh 'g++ main5.cpp -o output'
//       }
//     }
//     stage('Test') {
//       steps {
//         sh './output'
//       }
//     }
//     stage('Deploy') {
//       steps {
//         echo 'deploy'
//       }
//     }
//   }
//   post {
//     failure {
//       echo 'Pipeline failed'
//     }
//   }
// }



pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ main5.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        // Intentionally failing the test by executing a non-existent script
        sh './non_existent_script.sh'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
