# Synology-NAS

**DSM 7.2.1**

There is a list of NICs (symlinks) in a directory: /sys/class/net
10Gbps NIC is "eth2".
To find out the temperature of the 10G NIC, check the contents of the file: /sys/class/net/eth2/temperature

scemd.xml - DS923+ silent fan profile (10 Gbps NIC)

<fan_config period="20" threshold="6" type="DUAL_MODE_LOW" hibernation_speed="UNKNOWN">
	
	<disk_temperature fan_speed="01%40hz" action="NONE">0</disk_temperature>
	<disk_temperature fan_speed="10%40hz" action="NONE">41</disk_temperature>
	<disk_temperature fan_speed="20%40hz" action="NONE">43</disk_temperature>
	<disk_temperature fan_speed="35%40hz" action="NONE">45</disk_temperature>
	<disk_temperature fan_speed="40%40hz" action="NONE">47</disk_temperature>
	<disk_temperature fan_speed="50%40hz" action="NONE">49</disk_temperature>
	<disk_temperature fan_speed="70%40hz" action="NONE">54</disk_temperature>
	<disk_temperature fan_speed="99%40hz" action="NONE">58</disk_temperature>
	<disk_temperature fan_speed="99%40hz" action="SHUTDOWN">61</disk_temperature>

	<nic_temperature fan_speed="01%40hz" action="NONE">0</nic_temperature>
	<nic_temperature fan_speed="01%40hz" action="NONE">50</nic_temperature>
	<nic_temperature fan_speed="25%40hz" action="NONE">60</nic_temperature>
	<nic_temperature fan_speed="70%40hz" action="NONE">78</nic_temperature>
	<nic_temperature fan_speed="99%40hz" action="NONE">88</nic_temperature>
	<nic_temperature fan_speed="99%40hz" action="SHUTDOWN">100</nic_temperature>
 
</fan_config>
