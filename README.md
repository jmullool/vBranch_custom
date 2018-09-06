# vBranch_custom
vBranch FP container code and use case for deploying vRouter, vFW and vRouter+vFW service chain

0) Clone all files to local system in home (~) direcrtory:
    git clone 
    
1) Place day0 files on local web server that has IP reachability from NFVIS device:
    ISRV2.txt
    fortinet-config.txt
    
2) Place VNF package images (fortinert and ISRv) on Web server

3) Install docker application on unix system
  sudo setenforce 0
  yum install docker -y
  service docker start
  
4) Load container into docker image repo nso-4.6.1.3-vbranch-1.3-jjm_custom1.tar
   docker load -i nso-4.6.1.3-vbranch-1.3-jjm_custom1.tar

5) Run docker container- sharing files in home direcotry
   docker run -v ~/:/stuff --network host -p 80:80 -p 8080:8080 -p 830:830 -p 4000:4000 -p 2024:2024 -p 9191:9191 -p 9090:9090 -p 8989:8989 -it nso-4.6.1.3-vbranch-1.3-jjm_custom1 bash
   
6) gracefully quit out of the running container <Ctl-P> then <Ctl-Q>
    
7) re-enter the container with exec, first get container id with "docker ps"
   docker ps
   docker exec -it <id> bash
    
8) Update web URL location for day0 in ISR and fortinet deployment configs and for images in nfvo vnfds


   
  
    
