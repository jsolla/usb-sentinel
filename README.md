# USB Sentinel commandline tool
This tool is used to control the USB-SENTINEL device.

Once connected, the device presents itself to the system as a TTYACM device.

This tool just opens this TTYACM device and sends serial commands to it.


## Usage examples

Switch ON power on the slave USB port:

```
sentinelcmd /dev/ttyACM0 -on
```

Switch OFF power on the slave USB port:

```
sentinelcmd /dev/ttyACM0 -off
```

Power cycle (OFF-wait-ON) the slave USB port:
In this example the following sequence is performed:
- Power OFF slave USB port.
- Wait 5 seconds
- Power ON slave USB port

```
sentinelcmd /dev/ttyACM0 -cycle 5
```

