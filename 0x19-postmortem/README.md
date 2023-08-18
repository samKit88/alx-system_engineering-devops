# ALX Application-Server Outage Incident Report
####
The ALX Application-Server experienced a downtime on March 8, 2023. The outage was caused by a hardware failure. The server's hard drive failed, which resulted in the loss of data. The data was restored from a backup, and the server was brought back online.😊

####
## SUMMARY
> On November March 8, 2023 The server was unavailable for approximately 30 minutes, our application server was not functional. During this time, users were unable to login to their learning intranet site. The root cause of the problem was misspelled commands in the puppet configuration file. 
####
## TIMELINE _(all timelines are specified in East-African-Time)_
- 08:25 - puppet configuration applied
- 08:28 - outage begins
- 08:32 - the first customer reported the bug 
- 08:34 - the technical assistant teams allerted the software engineers team 
- 08:40 - server hardware, cpu and memory expanded
- 08:45 - server restart begins
- 08:50 - new server setup began 
- 09:02 - the incident escalated to the senior software engineers
- 09:05 - the team starts diagnosing and debugging using strace
- 09:08 - puppet file reconfigured
- 09:12 - server restart began
- 09:21 - 100% the server back online 
####
## ROOT CAUSE AND RESOLUTION
>At 08:25, a member of the DevOps team incorrectly entered commands in the Puppet manifest. This led to the configuration module being implemented without the approval of senior engineers. The incorrect command resulted in changing the file extensions of PHP Laravel files to 'phpp', which subsequently caused a complete breakdown of the application server.

This resulted in the inability to carry out any database requests. Simultaneously, the server experienced a surge in traffic, eventually rendering it unresponsive. At precisely 08:28, the service disruption commenced, persisting until the problem was addressed by senior engineers.

Ultimately, the resolution involved rectifying the issue by reconfiguring the Puppet modules and subsequently applying these corrected configurations to the main server.
####
## CORRECTIVE AND PREVENTIVE MEASURES
> Over the past seventy-two hours, we undertook a comprehensive analysis of our systems and engaged in extensive team deliberations. As a result of these discussions, we have taken the following measures to avert future breakdowns:

-Implementation of a server monitoring and notification system. We have established collaborative arrangements with software solutions such as dataDog and pagerDuty.

-Stringent monitoring of configurations intended for server deployment.

-Scheduled testing of server backups on a consistent basis.

-Ongoing monitoring of the operational well-being of our servers, applications, and networks.

-Regular updates to our software components.
####
__Reported__ __by__ __Samuel__ __Girma__
__ALX__ - __Holberton__
__Aug__ __18,__ __2023__
