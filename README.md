# x-session
Run RPi Desktop environment on Mac (or others) through X11 forwarding.

## How does this work
The RPi desktop, which is connected from a Mac (or others like Windows, Linux, etc.), is merged on the Mac (or others) as follows:
![](pics/HowRPiDesktopMergedOnMac.jpg)

## How to install
1. ```git clone https://github.com/UedaTakeyuki/x-session.git```
2. ```cd x-session```
3. ```sudo ./setup.sh```

Then, the ***x-session*** is symbolic-linked to /usr/local/bin.

## How to use
1. Open Terminal app on Mac (or others).
2. Connect to a RPi by ```ssh``` with ***-Y*** option like as follow:
```
ssh -Y pi@raspberrypi.local
```
3. Call ```x-session``` like as follow:
```
pi@raspberrypi:~ $ x-session
** Message: 11:11:58.420: main.vala:101: Session is LXDE-pi
** Message: 11:11:58.423: main.vala:102: DE is LXDE
** Message: 11:11:58.970: main.vala:133: log directory: /home/pi/.cache/lxsession/LXDE-pi
** Message: 11:11:58.971: main.vala:134: log path: /home/pi/.cache/lxsession/LXDE-pi/run.log
```

Note: ***-Y*** option for ```ssh``` command means that "```Enables trusted X11 forwarding.  Trusted X11 forwardings are not subjected to the X11 SECURITY extension con‐
             trols.```".
## History
- 2024.06.15 Created from scratch
