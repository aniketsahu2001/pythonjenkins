node {
  stage("Clone the project") {
    git branch: 'main', url: 'https://github.com/aniketsahu2001/pythonjenkins.git'
  }
  stage("Setting Virtual Environment") {
        sh 'python3 -m venv .'
  }
  stage("Installing") {
     sh './bin/pip install -r requirement.txt'
  }
  stage("Deploying") {
    sh 'python3 app1.py'
  }
  stage("Notifying") {
    emailext body: ' Deployed Successfully ' , 
        subject: 'App Deployed Status' , 
        to: 'aniketsahu473@gmail.com'
  }3
  .
}