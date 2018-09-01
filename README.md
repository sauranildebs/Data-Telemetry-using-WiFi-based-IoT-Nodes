# Communication-Relay-using-Wifi-Mesh
Communication Relay by creating a WiFi Mesh Network ( essentially making IoT Nodes) using ROS, and using that network for Data Telemetry, with Telemetry radios ( Ubiquiti Bullet, Ubiquiti Nanostation) being used as Access Points and Base stations. These are mounted on Drones (with provision for Autopilot using PixHawk modules) so as to facilitate large scale operations at remote locations, accompanied with an Android App. All of this is achieved without the use of an Active Internet Connection.


# The Complete Pipeline ( How, and the order in which the files work )
1. Drone checks connection to both the Nanostations using ping (chk_connection.py)
2. Whichever Nano the drone gets connected to, the transfer will take place with that Nano(dronecomm1.sh)
3. Data syncing is done with the respective nano (drone1.py)
4. It will ping the other nanostation ( chk_connection1.py)
5. Data syncing is done again with that Nano(The one with which the connection is established in the upper case). (dronecomm2.sh)
6. Again it will ping the first (chk_connection2.py)

# Login details for the WiFis and the RPis

Access Point 1

User: ubnt
Password: iiitd_ubnt
Preset IP Address: 192.168.1.158


Client:
User:ubnt
Password: ubnt123
IP Address: 192.168.1.160

Raspberry Pi:
user: iiitd
IP Address: 192.168.1.200
Password: test@123

Access Point 2
Wifi SSID: ubnt_IIITD
Password: ubiquiti_iiitd




