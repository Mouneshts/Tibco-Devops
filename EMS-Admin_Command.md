#### The following commands are used in Tibco EMS ADMIN
 

1. CREATE QUEUE:
Syntax

- **create queue [properties]**
- Example:
```bash
create queue Order.Q store=FileStore expiration=60000
```

2. CREATE TOPIC

Syntax:
**create topic [properties]**
Example:
```bash
create topic Order.Topic store=DbStore
```
3. CREATE BRIDGE
Syntax:

- **create bridge [properties]**
Examples:
```bash
create bridge queue:Source.Q queue:Target.Q
create bridge queue:Input.Q topic:Audit.T
```
4. MODIFY BRIDGE

Syntax:
**set bridge property=value**
Example:
```
set bridge queue:Order.Q queue:Archive.Q selector="priority > 5"
```
5. DELETE BRIDGE
Syntax:
**delete bridge**
Example:
```
delete bridge queue:Source.Q queue:Target.Q
```

6. SHOW COMMANDS

**show queue.
show topic.
show bridges**

7. COMMON PROPERTIES
**store=
maxmsgs=
maxbytes=
selector="JMS selector"
secure**
