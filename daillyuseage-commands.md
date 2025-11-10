# Tibco Admin Commands

## Domain Management

##### List all domains
tibcoadmin -domain

##### Create a new domain
tibcoadmin -domain <DomainName> -create

##### Delete a domain
tibcoadmin -domain <DomainName> -delete

### Application Management

##### Deploy an EAR file
AppManage -deploy -ear <AppName>.ear -app <AppName> -domain <DomainName> -user <User> -pw <Password>

##### Undeploy an application
AppManage -undeploy -app <AppName> -domain <DomainName> -user <User> -pw <Password>

##### List deployed applications
AppManage -list -domain <DomainName> -user <User> -pw <Password>

##### Export configuration of an application
AppManage -export -app <AppName> -domain <DomainName> -out <AppConfig.xml> -user <User> -pw <Password>

##### Import configuration
AppManage -import -app <AppName> -domain <DomainName> -in <AppConfig.xml> -user <User> -pw <Password>


## Start BW engine
```bash
bwengine -p <ProjectFolder> -t <TRAFilePath>
```

#### Stop BW engine (via OS or script)
```bash
kill -9 <PID>
```
##### Check BW version
```bash
bwengine -version
```

## EMS Server Commands

##### Start EMS server
```bash
tibemsd -config <tibemsd.conf>
```

##### Stop EMS server (CTRL + C or via OS kill)
```bash
kill -9 <PID>
```

##### Check EMS version
```bash
tibemsd -v
```

##### Connect to EMS
```bash
tibemsadmin -server tcp://localhost:7222 -user admin -password <pwd>
```

##### Inside EMS Admin prompt
```bash
show connections
show queues
show topics
show consumers
show producers
show routes
```
##### Create/Delete Queues/Topics
```bash
create queue TEST.Q
delete queue TEST.Q
create topic TEST.TOPIC
delete topic TEST.TOPIC
```

##### Manage Users & Permissions
```bash
create user test password test123
grant user test send queue=TEST.Q
revoke user test send queue=TEST.Q
```

##### EMS Monitoring
```bash
show server
show memory
show routes
show bridges
```
	
##### Start Hawk Agent
```bash
hawkagent &
```
### Hawk Configuration
	
##### View hawk agent properties
```bash
hawk_display -agent <AgentName>
```
##### Send test alert
```bash
hawk_sendalert -agent <AgentName> -alert TEST_ALERT
```
