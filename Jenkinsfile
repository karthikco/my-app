node{
  stage('SCM Checkout'){
    git 'https://github.com/karthikco/my-app'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }

}
