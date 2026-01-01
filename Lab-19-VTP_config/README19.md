#Overview

VTP (VLAN Trunking Protocol) is a Cisco-only protocol that is used to

share VLAN information between switches.

## 1. What is VTP?

VTP (VLAN Trunking Protocol) is a Cisco-only protocol that is used to

share VLAN information between switches.

Instead of creating the same VLANs on every switch, you can:

Create VLANs on one switch

Other switches learn them automatically

## 2.Why VTP exists

Without VTP:

You must create VLANs manually on every switch

Time-consuming

Easy to make mistakes

With VTP:

VLAN creation is centralized

Less manual work

##3.What information VTP shares

VTP shares:

VLAN ID (example: VLAN 10)

VLAN name (example: SALES)

VLAN status

❌ VTP does not share:

IP addresses

Port assignments

##4.Where VTP works

✔ Only between Cisco switches

✔ Only over trunk links

❌ Does not work on access ports

🔹 VTP Domain

A VTP domain is a group name.

Only switches with the same domain name can share VLANs

Different domain → no VLAN sharing

Example:

vtp domain AFRICA

## 5.VTP Modes

1.Server

Can create, delete, modify VLANs

Sends VLAN info to others

Default mode

2.Client

Cannot create VLANs

Learns VLANs from server

3️.Transparent (BEST PRACTICE)

Ignores VTP

VLANs are local only

Does not forward VTP messages

## 6.VTP Revision Number (IMPORTANT)

Every VLAN change increases a revision number

Switch with higher revision number wins

⚠️ Dangerous:

A wrong switch can delete all VLANs

1. Advantages of VTP

✔ Central VLAN management

✔ Less configuration

✔ Consistency

2. Disadvantages of VTP

❌ Risk of VLAN deletion

❌ Hard to troubleshoot

❌ Rarely used today

## 8.Best Practice (Modern Networks)

Most engineers:

Disable VTP

Use VTP Transparent

Create VLANs manually

vtp mode transparent

[![VTP_config Topology](Topology19.png.png)](Topology19.png)

##📥 Download Packet Tracer Topology

Click below to download the VTP_config lab topology:

👉 [Download VTP_config Packet Tracer Lab](https://github.com/USERNAME/REPO/raw/main/VTP_config.pkt)

##9.Lab Tasks

1. Create trunk link between every switch link connected 

2. Configure Vtp server on the Switch1 with vtp domain and password 

3. configure vtp client on the switch0 and switch3 with vtp domain and password

4. configure vtp transparent on the switch2 just with the domain 

domain = AFRICA 

Password = ali

NB: all the switches must have the same vtp domain and password and switch2 does not require passowrd

Lab configuration

Task1

Create trunk link between every switch link connected 

enter the interface then 
 
 switchport mode trunk
 
Task2

Configure Vtp server on the Switch1 with vtp domain and password 

Switch1

Switch(config)#vtp domain AFRICA

Changing VTP domain name from NULL to AFRICA

Switch(config)#vtp mode server

Device mode already VTP SERVER.

Switch(config)#vtp password ali

Setting device VLAN database password to ali
 
Task3

configure vtp client on the switch0 and switch3 with vtp domain and password

switch0

Switch(config)#vtp domain AFRICA

Domain name already set to AFRICA.

Switch(config)#vtp mode client

Setting device to VTP CLIENT mode.

Switch(config)#vtp passowrd ali

switch3

witch(config)#vtp domain AFRICA

Domain name already set to AFRICA.

Switch(config)#vtp mode client

Setting device to VTP CLIENT mode.

Switch(config)#vtp password ali

Task4

configure vtp transparent on the switch2 just with the domain

Switch(config)#vtp domain AFRICA

Domain name already set to AFRICA.

Switch(config)#vtp mode transparent

Setting device to VTP TRANSPARENT mode.

                       ##10 Command to check
                
				show vtp status
                
				show vlan brief


 
 
