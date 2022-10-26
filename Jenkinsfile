node('master') {
  def dockerTool = tool name: 'Docker_server', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
  withEnv(["DOCKER=${dockerTool}/bin"]) {
      dockerCmd "--version"
}

def dockerCmd(args) {
    sh "sudo ${DOCKER}/docker ${args}"
}
}
