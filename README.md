# jenkins-kube-plug-in


Link to Deploy Jenkins :

http://www.monkeylittle.com/blog/2017/02/07/deploying-jenkins-with-kubernetes.html

Link for reference kubernetes plugin

https://github.com/GoogleCloudPlatform/continuous-deployment-on-kubernetes

Docker hub link jnlp jenkins salve image 

https://hub.docker.com/r/jenkinsci/jnlp-slave/


Jenkins-UI service URL ::  http://jenkins.jenkins-dev:8080

Jenkins salve - jnlp [headless service URL] :: jenkins-discovery.jenkins-dev:50000

Arguments to pass to the command :: ${computer.jnlpmac} ${computer.name}

========================================================================================================================================

Kube-Plugin Global Configuaration
Cloud
Kubernetes
Name : RelianceJioKubernetes
Kubernetes URL : http://172.27.59.20:8080/r/projects/1a622/kubernetes
Kubernetes : Namespace 
Credentials : username & Password
Jenkins URL : http://172.27.59.108
Jenkins tunnel : 172.27.59.108:50000
Connection Timeout 0
Read Timeout  0
Container Cap 10

Images
Kubernetes Pod Template
Name : jenkins-jnlp-slave
Labels : jenkins-jnlp-slave
The name of the pod template to inherit from : keep blank
Containers
Name : jenkins-slave
Docker image : yuvrajh/jnlp-slave:lite1
Always pull image : user choice
Working directory : /home/jenkins
Command to run slave agent : keep blank
Arguments to pass to the command : ${computer.jnlpmac} ${computer.name}
Allocate pseudo-TTY : tick
EnvVars : as per user choice
Volumes
Host Path Volume
Host path : /var/run/docker.sock
Mount path : /var/run/docker.sock
