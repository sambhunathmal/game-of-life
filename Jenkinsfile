pipeline {
        agent {label 'JDK8' }
        stages {
              stage ('SoucrCode') {
                        steps {
                             git branch: 'spring1-develop', url: 'https://github.com/sambhunathmal/game-of-life.git'
                }
            }
        
               stage('Build the code') {
                         steps {   
                              sh 'mvn clean package'
                              }
                  }

                 stage('Archiving and Testing Results') {
                         steps {   
                               junit '**/surefire-reports/*.xml'
                               archiveArtifacts artifacts: '**/*.war', followSymlinks: false
                              } 

                   }
                
              }
         }
