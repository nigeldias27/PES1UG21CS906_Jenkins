pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES1UG21CS906-1'
        sh 'g++ main.cpp -o ouput'
      }
    }
    stage('Test'){
      steps{
          sh './ouput'
      }
    }
    stage('Deploy'){
      steps{
          echo 'Deploy'
      }
    }
    
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
