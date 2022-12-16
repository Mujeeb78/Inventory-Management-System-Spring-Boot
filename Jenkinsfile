node('Slave') {
    stage ('checkout code'){
          git credentialsId: '3801a20d-9cbd-4fb7-b8a3-837ecbea5ef6', url: 'https://github.com/Mujeeb78/Inventory-Management-System-Spring-Boot'
    }

    stage ('Build'){
        sh "mvn clean install -Dmaven.test.skip=true"
    }

 

    stage ('Test Cases Execution'){
        sh "mvn clean install -Dmaven.test.skip=true"
    }
}
