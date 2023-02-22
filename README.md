# ADB SHELL
 
[More commands here](https://technastic.com/adb-shell-commands-list/#adb_shell_pm_uninstall)

* to Show All devices
```bash
cmd# adb shell
```

* To connect device
```bash
adb connect <ip-address-of-device>
```
* to open device as a root user
```bash
adb root 
or shell@LoneWolf:/ su
```

*  if you want to list the system apps only
```bash
adb shell pm list packages -s
```

*  In order to list all third-party apps
```bash
adb shell pm list packages -3
```

*  Do you want ADB Shell to show the list of all enabled or disabled apps on your device, try the command with parameters like ‘-d‘ (for disabled apps), ‘-e‘ (for enabled apps), and ‘-u‘ (for uninstalled apps).

```bash
adb shell pm list packages -d

adb shell pm list packages -e

adb shell pm list packages -u
```

*  To list app packages with specific keyword filters.
```bash
adb shell pm list packages <keywords>
```
*  adb shell pm uninstall
> This is really a very useful ADB Shell command. Using this, you can easily uninstall unwanted system apps. To be able to execute it, you must issue ‘adb shell‘ command first. You can then use pm uninstall -k --user 0 or pm uninstall --user 0 followed by the Android app package name as shown below.
```bash
pm uninstall -k --user 0 com.facebook.appmanager
```
> -k: Keep the app data and cache after package removal. If you want the app data to be cleared as well, use the following

```bash
pm uninstall --user 0 com.android.chrome
```

* install apk using cmd 

```bash 
adb install "<location-0f-file>"      #D:\GOW asc\vp_app.apk
```

* Run app

```bash 
monkey -p com.rishabhgarg60.videoplayer_app2 1
```

* disabled any app (some app require root permission)
```bash
pm disable-user user 0 cn.zeasn.launcher.vstoresubclient.ktc

```

* to enable again

```bash
pm enable cn.zeasn.launcher.vstoresubclient.ktc
```
* Read only file-system error
> Not all phones and versions of android have things mounted the same.
Limiting options when remounting would be best.

Simply remount as rw (Read/Write):
```bash
# mount -o rw,remount /system
```
> Once you are done making changes, remount to ro (read-only):

```bash
# mount -o ro,remount /system
```
* How I connect my Samsung A30s using ADB
>I enabled first Wireless debugging in my phone. Then i tried one command  `adb pair [host]:[port] [code]` to connect directly to adb (get host, port and code details in Wireless debugging option ) or else you can try npm package to install qr library. `npm i adb-wifi -g` then run `adb-wifi`. next step to connect device to adb `adb connect [host]:[port]`, check device by running `adb devices`.  
```bash

```
# Android Tv 

[atv11_bootanimation](https://github.com/khurramrizvi/atv11_bootanimation)

[Push and pull](https://www.thecustomdroid.com/adb-push-pull-commands/)

[Android Forum](https://forum.xda-developers.com/c/android-tv.4276/)

[Projectivity launcher](https://forum.xda-developers.com/t/app-android-tv-projectivy-launcher.4436549/)