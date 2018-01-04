pipeline
{
  node('build-node')
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
        sh 'env > env.txt'
        for (String i : readFile('env.txt').split("\r?\n")) {
                              println i
                              }
        echo 'current build result is: env'
      }
    }
  }
}


      
