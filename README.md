This project is based on this work: http://www.bford.info/pub/net/p2pnat/index.html

This will build on Linux or OSX.  Make sure you have gcc installed.

to build, run

    make

Before running, make sure you have an LTE modem connected to its network
and has an IP address.  Then, determine its network name.  On Linux, this will
likely be "wwan0".  On Mac, its prbobably "en10" or "en11".  BE SURE TO
DISCONNECT ANY OTHER CONNECTED NICS LIKE WIFI OR ETHERNET.

You will need to run this command on two separate computers or VMs with
separate LTE modems connected to each.

To execute, run the command

    ./natclient -d wwan0 -s 54.173.71.197 -p 9234

Where wwan0 is the LTE device name, 54.173.71.197:9234 are the IP/port for
the rendezvous server.  These are the defaults for the AWS server.

You will get a bunch of output detailing round-trip ping times and
statistics of those ping times.  Each output will detail if it was able to send
data over public or private ip/port tuples.
