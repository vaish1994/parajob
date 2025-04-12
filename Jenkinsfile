pipeline {
  agent any
  parameters {
             string (name: 'maven_version', defaultValue: '3.9.4', description: 'Pass the value of maven')
             string (name: 'terraform_version', defaultValue: '1.8.3', description: 'Pass the value of terraform')
  }
  stages {
         stage ('download maven') {
                steps {
                sh '''
                cd /tmp
                sudo wget https://dlcdn.apache.org/maven/maven-3/${maven_version}/binaries/apache-maven-$maven_version-bin.tar.gz
                '''
                }
         }

        stage ('download terraform') {
                        steps {
                        sh '''
                        cd /tmp
                        sudo wget https://releases.hashicorp.com/terraform/${terraform_version}/terraform_$(terraform_version)_linux.amd64.zip
                        '''
                        }
                 }

         }
}