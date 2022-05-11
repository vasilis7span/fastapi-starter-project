pipeline{
 agent any
  
  stages{
    stage('clone') {
      steps{
        sh '''
         echo 'Clone'
        '''
      }
    }
    stage('test'){
      steps{
        sh '''
          cp app/.env.example app/.env

          docker-compose down --volumes

          docker-compose up -d --build

          python3 -m venv favenv

          source favenv/bin/activate

          pip install -r requirements.txt

          pytest
        '''
      }
    }
  }
}
