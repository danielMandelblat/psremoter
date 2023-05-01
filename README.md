# PSRemoteExecuter
## _Suitable for Windows and Linux platforms_

This package will help you to execute remote PowerSell script on other Windows platforms in your domain. 

## Features

- Execute local PowerShell scripts
- Execute remote PowerShell scripts (Using invoke-command PS command)


##Using
install PSRemoter using pip:<br>
pip install psremoter

powershell=False (default) execute as batch script
```
from psremoter import psremoter
exec= psremoter(hostname="hostname", username="username" , password='password', domain='myDomain', command="hostname", powershell=True)

#Execute command on remote host
exec.remote_execution()

#Read execution status
print(exec.status) #True

#Read return code
print(exec.return_code) #0 

#Read console output
print(exec.output) #DnsServer01
````
