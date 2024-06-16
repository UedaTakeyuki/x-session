# x-session
Run RPi Desktop environment on Mac (or other Hosts) through X11 forwarding.

## How does this work
The RPi desktop, which is connected from a Mac (or other Hosts like Windows, Linux, etc.), is merged on the Mac (or others) as follows:
![](pics/HowRPiDesktopMergedOnMac.jpg)

## How to install
1. ```git clone https://github.com/UedaTakeyuki/x-session.git```
2. ```cd x-session```
3. ```sudo ./setup.sh```

Then, the ***x-session*** is symbolic-linked to /usr/local/bin.

## How to use
1. Open the Terminal app on Mac (or other Hosts).
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

Note: ***-Y*** option for ```ssh``` command means that "```Enables trusted X11 forwarding.```".

## Requirement
- X11 is running on both an RPi and (Mac or other Hosts)
  - RPi:  
    By default X11 is running except for ***Waylang*** is selected.
  - Mac:  
    X11 available with [XQuartz](https://www.xquartz.org/)
  - Windows:  
    I'm not familiar with Windows because I don't use Windows after Windows 7 due to my anger at the continuous meaningless changes. In my memory about 
 Windows 7, the X11 was available with Cygnus but I'm not sure about recent Windows.
  - Linux:  
    By default X11 is running except for ***Waylang*** is selected.

## History
- 2024.06.15 Created from scratch
