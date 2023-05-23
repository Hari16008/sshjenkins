node{
  def remote = [:]
  remote.name = 'oraclevm'
  remote.host = '152.67.160.182'
  remote.user = 'opc'
  remote.password = 'Muzammil073#'
  remote.allowAnyHosts = true
    stage('checkout') {
           checkout scm
  }  
  stage('Remote SSH') {
   // writeFile file: 'Jenkinsfilescript.sh', text: 'ls -lrt'
   // sshScript remote: remote, script: "Jenkinsfilescript.sh"
    sshCommand remote : remote, command: "pwd"
    sshCommand remote : remote, command:  mkdir "Hari16008"
      sshCommand remote : remote, command: "cd /opc/home"
    sshCommand remote : remote, command: "pwd"
      sshCommand remote : remote, command: "ls -lrt"
  }     
  }  
 stage('step1'){
  sshPut remote: remote, from: 'Jenkinsfilescript.sh', into: '/home/opc'
 }
  stage('step2'){
 sshCommand remote: remote, command: "sudo sh /home/opc/Jenkinsfilescript.sh"
 }
  stage('step2'){
 sshCommand remote: remote, command: "pwd"
 }
  stage('step3'){
 sshCommand remote: remote, command: "mv /home/opc/Jenkinsfilescript.sh  /home/opc/Hari16008/"
 }
}
        }
