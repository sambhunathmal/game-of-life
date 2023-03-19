node('JDK8') {
        stage('SoucrCode') {
              git branch:'spring1-develop',url:https://github.com/sambhunathmal/game-of-life.git
        }
        
        stage('Build the code') {
              sh 'mvn clean package'
        }

        stage('Archiving and Testing Results') {
              junit '**/surefire-reports/*.xml'
              archiveArtifacts artifacts: '**/*.war', followSymlinks: false
       }

}
