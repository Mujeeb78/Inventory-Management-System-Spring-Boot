try {
node('Slave'){
    stage('Code Checkout'){
        git credentialsId: '3801a20d-9cbd-4fb7-b8a3-837ecbea5ef6', url: 'https://github.com/Mujeeb78/Inventory-Management-System-Spring-Boot
'
            }
   
   stage('Build & Test Automation'){
      sh """ls -lart
          mvn clean install 
         """
   }
   stage ('Email notification'){
       emailext body: 'Build is passed', subject: 'Build Status', to: 'chaitanyapriya1211@gmail.com'
   }
}
}
catch (e){
         echo "Handling Exception !!!!"
         currentBuild.result = "FAILURE"
         emailext body: 'Build failed', subject: 'Build status', to: 'mujeeb9742@gmail.com'
         throw e
}
