LoadMaster Template
===================

This template use the IPVS-MIB and B100-MIB to discover and manage LoadMaster.

Items
-----
  * CPU: System / User / SoftIRQ / Nice / Interrupt / Idle
  * Load Average: 1min / 5min / 15min
  * Memory: Used / Shared / Buffer / Cached / Free / Total
  * TPS: TPS / SSL TPS
  * Connections: Number of connections of LoadMaster.
  * Total Virtual Services: VirtualService number of LoadMaster.
  * HA State: HA State.
  * Network Traffic: Packet / byte / bit number of input and output of the LoadMaster.
  * Discovery: Network Interface.
    * Packets / Traffic / Interface Speed
  * Discovery: Virtual Service.
    * Active Connections / Connections / Traffic / State
  * Discovery: Real Server.
    * Active Connections / Connections / Traffic / State

Triggers
--------
  * **[WARNING]** => HA State Change.
  * **[INFORMATION]** => Discovery: Virtual Service State is Disabled
  * **[INFORMATION]** => Discovery: Virtual Service State is In Service
  * **[INFORMATION]** => Discovery: Virtual Service State is Redirect
  * **[WARNING]** => Discovery: Virtual Service State is Sorry
  * **[WARNING]** => Discovery: Virtual Service State is Errormsg
  * **[HIGH]** => Discovery: Virtual Service State is failed
  * **[HIGH]** => Discovery: Virtual Service State is Out Of Service


Graphs
------
  * CPU Util: CPU Utilization Infomations (CPU x 100 %. 2CPU = 200%)
  * Load Average: Load Average Infomations.
  * Memory: Memory Usage Infomations.
  * Connections: Number of connections of LoadMaster.
  * TPS: TPS information.
  * Total Virtual Services: VirtualService number of LoadMaster.
  * Total Network Packets: Network Packets of LoadMaster.
  * Total Network Traffic (Bit): Network Traffic(Bit/sec) of Loadmaster.
  * Total Network Traffic (Byte): Network Traffic(Byte/sec) of Loadmaster.
  * HA State: HA State ( 1 = HA, 0 = Not HA )
  * Discovery: Network Interface.
    * Packets / Traffic / Interface Speed
  * Discovery: Virtual Service.
    * Active Connections / Connections / Traffic / State
  * Discovery: Real Server.
    * Active Connections / Connections / Traffic / State

Installation
------------

1. SNMP settings to LoadMaster.
2. LoadMaster Host added to ZABBIX.
3. SNMP interface added to the LoadMaster Host.
4. Template import.
5. Use the template.

Requirements
------------

 All this templates was tested for Zabbix 2.2.0 and LoadMaster Version 7 and higher.
 SNMP configuration of LoadMaster.

License
-------

 Released under the [MIT license](http://opensource.org/licenses/mit-license.php).

### Copyright

  Copyright (C) 2014 BeGoodTechnology Inc. All Rights Reserved.


