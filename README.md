PenE
====

[PEN](http://siag.nu/pen/) load balancer (LB) management.

# What is
Meant to handle the disposal of workers within a PEN cluster. 

Together with a monitoring tool, PenE provides a simple means to achieve 
**high availability** (HA).


# How
There is no restriction about the monitoring tool to be used, just use PenE as 
the (external) command to add/remove alerts (aka triggers) for a given worker. 
PenE will then decide if the worker can be added/removed from the cluster based
on the presence/absence of two features: *triggers* and *validation tag*.

## Triggers      
A means of assigning an issue to a worker (e.g. worker overloaded).
## Validation tag
Invalidating a worker will (until an admin's explicit validation) take it apart 
from the LB system.

The validation tag appears as the top priority criteria, whose assessment will
decide whether the trigger evaluation phase will be taken into account.


# Incoming improvements
## Support
 * LVS load balancer management.

## Documentation
 * PenE <-> Zabbix/Nagios integration example.
