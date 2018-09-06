# vBranch_custom
vBranch FP container code and use case for deploying vRouter, vFW and vRouter+vFW service chain

0) Pull all files to lcoal system:
    git clone 
    
1) Place day0 on local web server that has IP reachability from NFVIS device:
    ISRV2.txt
    fortinet-config.txt
    
2) Place VNF images (fortinert and ISRv) on Web server

3) Install docker application on unix system
  sudo setenforce 0
  yum install docker -y
  service docker start
  
4) Copy docker container file to local system (nso-4.6.1.3-vbranch-1.3-jjm_custom1.tar)

5) Load the contianer into docker image repo:
   
  
    
