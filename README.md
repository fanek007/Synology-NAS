# Synology NAS tweaks


## Check 10GbE NIC (E10G22-T1-Mini) temperature in DSM 7.2.1

<p>
	There is a list of NICs in a directory: /sys/class/net<BR>
	10GbE NIC is "eth2".<BR>
	<BR>
	To find out the temperature of the 10GbE NIC, check the contents of the file: /sys/class/net/eth2/temperature
</p>


## DS923+ silent fan profile (E10G22-T1-Mini 10GbE NIC)


<p>
/usr/syno/etc.defaults/scemd.xml<BR>
/usr/syno/etc/scemd.xml
</p>

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

                <m2_temperature fan_speed="01%40hz" action="NONE">0</m2_temperature>
                <m2_temperature fan_speed="25%40hz" action="NONE">48</m2_temperature>
                <m2_temperature fan_speed="50%40hz" action="NONE">56</m2_temperature>
                <m2_temperature fan_speed="75%40hz" action="NONE">64</m2_temperature>
                <m2_temperature fan_speed="99%40hz" action="SHUTDOWN">70</m2_temperature>

                <cpu_temperature fan_speed="01%40hz" action="NONE">0</cpu_temperature>
                <cpu_temperature fan_speed="10%40hz" action="NONE">57</cpu_temperature>
                <cpu_temperature fan_speed="20%40hz" action="NONE">62</cpu_temperature>
                <cpu_temperature fan_speed="50%40hz" action="NONE">65</cpu_temperature>
                <cpu_temperature fan_speed="70%40hz" action="NONE">78</cpu_temperature>
                <cpu_temperature fan_speed="99%40hz" action="NONE">86</cpu_temperature>
                <cpu_temperature fan_speed="99%40hz" action="SHUTDOWN">95</cpu_temperature>

                <nic_temperature fan_speed="01%40hz" action="NONE">0</nic_temperature>
                <nic_temperature fan_speed="01%40hz" action="NONE">50</nic_temperature>
                <nic_temperature fan_speed="25%40hz" action="NONE">60</nic_temperature>
                <nic_temperature fan_speed="70%40hz" action="NONE">78</nic_temperature>
                <nic_temperature fan_speed="99%40hz" action="NONE">88</nic_temperature>
                <nic_temperature fan_speed="99%40hz" action="SHUTDOWN">100</nic_temperature>

</fan_config>
