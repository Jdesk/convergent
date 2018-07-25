---


---

<p>Rancher-Server</p>
<p>Linode: 2GB / 1VCPU - $10.00 / month<br>
RDS:  t2micro with 20gb ssd general purpose storage - $14.71 / month<br>
Rancher-Host-1 (Rocket-chat) - Linode 8GB - $40.00 / Month<br>
Rancher-Host-2 (Rocket-chat) - Linode 8GB - $40.00 / Month</p>
<p>Rancher-staging-host-1 (rocket-chat staging) - Linode 2GB $10.00 / month</p>
<p>Total Cost for rancher environment - $114.71</p>
<p>Continous Integration:<br>
Dockercloud - $7 / month with 1 private repo</p>
<p>Redundancy / Failover - All rocketchat hosts will be loadbalanced using HAProxy which will send traffic to nodes that are in an available state - healthchecks will be setup within Rancher</p>
<p>Backups - Host backups handled by Linode, Mongo Backups handled by Atlas.</p>
<p>Server Security - Best security practices will be used on all resources.   I will use UFW and IPtables to configure security on each host and rancher server.</p>
<p>RDS Security - Rancher Server database will only be accessible by rancher-server IP.</p>
<p>Server Monitoring - all hosts will have monitoring within rancher - for individual container monitoring, we will use weave-scope.  There is no cost for either of these monitoring solutions.  Weave scope will be accessible via a URL endpoint that I configure.  URL endpoint will be password protected.</p>
<p>DNS - I will continue to use cloudflare for DNS</p>
<p>SSL - I will use letsencrypt and setup auto-renewal and management of ssl certificates within rancher</p>
<p>Cacheing - will be setup at the host level using nginx best cacheing practices</p>
<p>Production / Staging Relationship - Production and staging environments will be setup within rancher and linked to specific branches in the github repository.  Eg. develop branch will be linked via CI pipeline (docker cloud) to rancher development environment.   Each environment will have it’s own database within the master rancher-server database.   Creating environments in rancher will help alleviate costs associated with having multiple database instances and multiple server instances.</p>

