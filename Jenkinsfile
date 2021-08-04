node ('MASTER') {
    stage ('scm') {
        git 'https://github.com/mahesh-source/openmrs-core.git'
    }
    stage ('build') {
        sh 'mvn clean package'
    }
    stage ('post build') {
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}