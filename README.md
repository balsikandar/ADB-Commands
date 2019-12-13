## Most useful ADB commands
This Repo contains a list of most useful everyday ADB commands. 

### ADB Pull and Push files from Device to PC

First check all the connected devices using
```
adb devices
```

If multiple devices are connected check below image then use command with device id

<img src = https://github.com/balsikandar/ADB-Commands/blob/master/assets/devices-list.png>

Run schell script with Device Id
```
adb -s RZ8M60W2LCH shell
```

Since we're connected to device now we can browse code using commands like **ls, pwd, cd**
```
$ ls

$ cd sdcard/ 
```

Finally once you find the file you want to pull just use pull command
```
e.g: adb pull /sdcard/screenshots/screen.png 
```

### ADB am (Activity Manager)
Activity Manager *(am)* can be used to stuffs like broadcasting intent to start an activity or making calls etc...

#### Making a call
```
adb shell am start -a android.intent.action.CALL -d tel:88******97
```

#### Open Google Map
```
adb shell am start -a android.intent.action.VIEW -d 'geo:28.65381,77.22897'
```

#### Broadcasting an Intent
```
adb shell am broadcast android.net.conn.CONNECTIVITY_CHANGE
```

### ADB Screen Record
Record video while testing or debugging your app.

#### Record screen video on device
```
adb shell screenrecord /path-on-device/recording.mp4
```

#### We can set *time-limit* for minimum recording time
```
adb shell screenrecord /sdcard/recording.mp4 --time-limit 20
```

#### To check all the available options
```
adb shell screenrecord --help
```
