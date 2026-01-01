Configure access point in Cisco packet tracer

In this lab, we will configure a wireless access point in the Cisco packet tracer, and devices like phones, tabs, and laptops will be connected to the network.

A wireless access point allows devices to connect to the network wirelessly so to connect different devices to the access point, we have to configure the access point for basic settings.

We can configure port 1 of the access point for the wireless-related settings.

(images/TopologyA.png)](images/TopologyA.png)


By default, SSID is configured as default and authentication is disabled and the same is configured on end devices available so we just have to add the devices to the map and they will connect to the access point immediately because the devices are preconfigured with the required settings however If we have changed the SSID and enabled the authentication then we have to connect the device with the available SSID and also for authentication, the password must be entered.

(images/TopologyB.png)](images/TopologyB.png)


To connect the Laptop or PC, we have to remove the Ethernet module and add the wireless module so these devices can support wireless connectivity while the other two devices have the wireless module preconfigured.

[![access_point_config Topology](images/TopologyC.png)](images/TopologyC.png)

##📥 Download Packet Tracer Topology

Click below to download the access_point_config lab topology:

👉 [Download access_point_config Packet Tracer Lab](https://github.com/USERNAME/REPO/raw/main/access_point_config.pkt)

In the above image, you can see the 3 different devices are connected to the access point however they are not yet assigned the IP address.

Usually, routers provide more functionality as compared to access points e.g. routers can be configured with an access list and many more services like the quality of service, DNS, MAC address filtering, etc.

Routers available these days in the market have the ability to behave like an access point as well but normally in a large organization, access points are preferred due to their specific role and ease of configuration.

In big organizations, multiple access points are used to cover a large area so that access can be provided to users at every location.

The wireless router has the ability to assign dynamic IP addresses however repeater cannot assign IP addresses so to establish connectivity between different devices; we have to assign an IP address from the same network range.

If we want to assign the IP addresses dynamically then we can either add a wireless router to the network or configure a DHCP server.

We can also define the wireless range on the access point. By default, the access point is configured with a range of 140 meters so to reduce or increase the range, we can modify this setting.
