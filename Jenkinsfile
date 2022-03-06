pipeline {
            agent any 
  stages {
    stage ('checkout code ') {
      steps {
    	         git(url: 'https://github.com/vivek4545/Calculater-App-Python.git', branch: 'master', credentialsId: 'github_cred', poll: true)
      }}
    
  
  stage ('build code  ') {
      steps {
    	        sh "source calculator/bin/activate  &&  pip install -r requirements.txt"
      }} 
  
    stage('test code') {
      steps {
        sh " source calculator/bin/activate && flake8 --exclude=venv* --statistics &&  pytest -v --cov=calculator "
    }}  
  }}
