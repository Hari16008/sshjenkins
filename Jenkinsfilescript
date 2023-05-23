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
   // writeFile file: 'abc.sh', text: 'ls -lrt'
   // sshScript remote: remote, script: "Jenkinsfilescript.sh"
    sshCommand remote : remote, command: "pwd"
    sshCommand remote : remote, command:  mkdir "Hari16008"
      sshCommand remote : remote, command: "cd /opc/home"
    sshCommand remote : remote, command: "pwd"
      sshCommand remote : remote, command: "ls -lrt"
  }     
  stage('Remote SSH 2') {
   sshScript remote: remote, script: "/home/opc/jenkinsfilescript.sh"
  }  
 stage('Remote SSH 3') {
    writeFile file: 'Jenkinsfilescript.sh', text: 'ls -lrt'
    sshPut remote: remote, from: 'Jenkinsfilescript.sh', into: '/home/opc/Hari16008'
  }
}
        }
