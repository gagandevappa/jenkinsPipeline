pipeline
{
  agent any
  stages
  {
    stage('scm')
    {
      steps
      {
        checkout scm
        archiveArtifacts artifacts:'*', fingerprint: true
        echo 'scm completed'
      }
    }
    stage('build')
    {
      steps
      {
        echo 'Build completed'
      }
    }
    stage('test')
    {
      steps
      {
        echo 'Testing completed'
      }
    }
    stage('docker')
    {
      steps
      {
        echo 'dockerization completed'
        echo 'current build result is: ${currentBuild.result}'
      }
    }
  }
}


      
