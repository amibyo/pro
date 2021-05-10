pipeline{
    agent any
             stage('checkout II')
                            {
                         echo 'Hello, git'
                         git 'https://github.com/ElferjeniDevops/maven/'
                        }
                
             stage('Example Build II') 
                          { 
                          echo 'Hello, Maven'
                          sh 'mvn --version'
                        }
             stage('phase de validation de code  II') 
                          { 
                          echo 'phase de validation de code '
                          sh 'mvn validate'
                        }
             stage('phase de compilation II') 
                          { 
                          echo 'phase de compilation '
                          sh 'mvn compile'
                        }
             stage('phase de tesT II') 
                          { 
                          echo 'phase de test '
                          sh 'mvn test'
                  
                             }
              stage ('Testing Stage II') {

          
             post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
             stage('phase de packetage') 
                          { 
                          echo 'phase de packetage  '
                          sh 'mvn package'
                        }
             stage('phase d_intallation de pachake dans votre RL') 
                          { 
                          echo 'phase d_intallation de pachake dans votre RL '
                          sh 'mvn validate'
                        }
               stage('phase de deploiement d_un artefact dans le referentiel distant') 
                          { 
                          echo 'phase de déploiement d_un artefact dans le référentiel distant'
                         sh "mvn deploy"
                        }
 }
      
     
