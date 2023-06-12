# Eclipse Mosquitto Broker running on PC

- [eclipse mosquitto broker download site](https://mosquitto.org/)
- [mqtt explorer download site](http://mqtt-explorer.com/)
- [setup mosquitto broker and mqtt explorer on PC by insights in automation](https://www.youtube.com/watch?v=Zvz8LkQpyk0)
- [understanding and configuring mosquitto logging by Steve's internet guide](http://www.steves-internet-guide.com/mosquitto-logging/)

Create a folder called `DevMosquitto` in the root directory.

Install the Mosquitto broker in the `DevMosquitto` folder without the run as a service option.

Open a `cmd` terminal and make the working directory `DevMosquitto`. Then type the following commands:

```bash
# From the DevMosquitto folder run the broker in verbose mode
mosquitto -v
# Open another cmd terminal and run netstat
netstat -a
```
The netstat output shows that the broker is in local mode

```bash
Proto  Local Address          Foreign Address        State
TCP    127.0.0.1:1883         LAPTOP-0815A3MT:0      LISTENING
```


We must edit the config file so the broker will listen on all tcp addresses.

In the DevMosquitto folder open the `mosquitto.conf` file with notepad.
Edit the two areas as shown below and save. Setting `allow_anonymous` to true allows no need to authenticate. Setting the listener as shown allows the broker to listen to all tcp/ip addresses.

```bash
# acl_file

allow_anonymous true

# allow_zero_length_clientid

...

# listener port-number [ip address/host name/unix socket path]

listener 1883 0.0.0.0

# By default, a listener will attempt to listen on all supported IP protocol
```

Stop the running broker and restart this time using the edited config file.

```bash
# From the DevMosquitto folder run the broker in verbose mode using the config file
mosquitto -v -c mosquitto.conf
# Open another cmd terminal and run netstat
netstat -a
```
The netstat output shows that the broker is now listening to all tcp/ip addresses.

```bash
Proto  Local Address          Foreign Address        State
TCP    0.0.0.0:1883         LAPTOP-0815A3MT:0      LISTENING
```
Now we must know the ip address of our PC

```bash
# open a cmd terminal in admin mode
ipconfig /all
```
Look for the Ipv4 address of the NIC (Network Interface Card) that is connecting the PC to the network.

With the Mosquitto broker running on the PC start the MQTT Explorer client and connect to the running Mosquitto broker using the ip address of the PC NIC.