pipeline
{
  agent any
  tools
  {
    gradle 'Gradle'
    jdk 'JDK11'
  }
  
  stages
  {
    stage('Checkout')
    {
      steps
      {
        git branch:'master',url:'https://github.com/yasasvini2818/gradlepipe.git'
      }
    }
    stage('Build')
    {
      steps
      {
        sh'gradle build'
      }
    }
    stage('Test')
    {
      steps
      {
        sh'gradle run'
      }
    }
    stage('Run Application')
    {
      steps
      {
        sh'gradle run'
      }
    }
  }
  post
  {
    success
    {
      echo 'Build successful'
    }
    failure
    {
     echo 'Build failed'
   }
 }
}
