# AlertDashboard
##  Use DeepSee to create a dashboard to show abnormal conditions of Production operation.
######   Device: Raspberry Pi 
######   Version:IRIS for UNIX (Ubuntu Server LTS for ARM64 Containers) 2021.1 (Build 205U) 
1.  open Management Portal,Create new namespace "BI"
1.  open your studio,and Switch to namespace "BI",
2.  Download all contents under the BI folder，import all  OR Import BI.xml and BI/Dashbord/BI-Dashbord-AlertDashboard.dashboard.xml code file from studio and compile
4.  open Management Portal，switch namespace “BI”，
5.  select【System Explorer】-->【GLOBALS】-->use "import" button,select "export.gof"
6.  go to production,start "BI.PD.AlertProduction"
7.  open SMP in namespace BI Analytics > User Portal >  Alert Dashboard
8.  success!!!
###  Dashboard data is refreshed every 5s
## Docker
The example works in namespace USER    
Step 1...5 are done during container start     
Step 6.  start production"BI.PD.AlertProduction"    
http://localhost:42773/csp/user/EnsPortal.ProductionConfig.zen?PRODUCTION=BI.PD.AlertProduction     
Step 7.  open SMP in namespace BI Analytics > User Portal >  Alert Dashboard     
http://localhost:42773/csp/user/_DeepSee.UserPortal.DashboardViewer.zen?DASHBOARD=BI/Dashbord/AlertDashboard.dashboard      

### Prerequisites
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.
### Installation
Clone/git pull the repo into any local directory
```
$ git clone https://github.com/rcemper/PR_AlertDashboard.git
```
```
$ docker compose up -d && docker compose logs -f
```
To open IRIS Terminal do:
```
$ docker-compose exec iris iris session iris
USER>
```
or using **WebTerminal**    

http://localhost:42773/terminal/
     
To access IRIS System Management Portal     
    
http://localhost:42773/csp/sys/UtilHome.csp
  




