pipeline {
            agent any 
  stages {
    stage ('checkout code ') {
      steps {
    	         git(url: 'https://github.com/vivek4545/Calculater-App-Python.git', branch: 'master', credentialsId: 'github_cred', poll: true)
      }}
    
  
  stage ('build code  ') {
      steps {
    	        sh " cp * /home/ansible1/Calculator-App-Python/ && cd /home/ansible1/Calculator-App-Python/calculator && source bin/activate && cd .. &&  pip install -r requirements.txt"
      }} 
  
    stage('test code') {
      steps {
        sh " cd /home/ansible1/Calculator-App-Python/calculator && source bin/activate && cd .. && flake8 --exclude=venv* --statistics &&  pytest -v --cov=calculator "
    }}  
  }}
