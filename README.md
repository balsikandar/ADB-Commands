## Most useful ADB commands
This Repo contains a list of most useful everyday ADB commands. 

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
