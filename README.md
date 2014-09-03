firefoxos
=========

notes and work on firefoxos

### flame info

https://developer.mozilla.org/en-US/Firefox_OS/Developer_phone_guide/Flame

### bugzilla

#### adb devices empty on os 2.0

https://bugzilla.mozilla.org/show_bug.cgi?id=1060427

ok on 2.1, unresponsive on 2.0 (update, now fixed)

### adb

    adb devices
    adb kill-server

or add to alias

    flushadb="adb kill-server && adb start-server"

port forward

    adb forward tcp:6000 tcp:6000

### fixing adb

http://stackoverflow.com/questions/7135999/adb-not-finding-my-device-phone-macos-x

If you need adb back for
any reason (like, reflashing the 2.1 to have it working again in normal
condition) you can reboot in recovery mode, do a factory reset (I'm not sure
this step it's actually required) and when you reboot after that, type this on
your linux console:

    adb wait-for-device && adb root && adb wait-for-device && adb shell stop b2g

this way you can use adb to shallow flash another version of b2g.

### irc

https://groups.google.com/forum/#!forum/mozilla.dev.b2g

https://groups.google.com/forum/#!topic/mozilla.mozillians/gzekUpLo0MU

### tcp

https://wiki.mozilla.org/FirefoxOS/TCP/Flashing_the_Flatfish_bootloader

### firefoxos wiki

https://wiki.mozilla.org/FirefoxOS

### installing

http://kaustavdm.in/2014/08/connect-firefox-os-spreadtrum-device-adb.html
https://developer.mozilla.org/en-US/Firefox_OS/Installing_on_a_mobile_device
