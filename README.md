# development tools for Android/iOS.
Utility command line tools for Android/iOS development.

## Android
### adb_screenrecord_pull
Execute screenrecord on your Android device and pull the recorded file to local directory.

#### Usage
```bash
adb_screenrecord_pull myMovie.mp4
```

#### Requirements
- adb

### adb_screencap_pull
Execute screen capture on your Android device and pull the captured file to local directory.

#### Usage
```bash
adb_screencap_pull myScreenShot.png
```

#### Requirements
- adb


## Android and iOS
### mpeg2gif
Generates animated GIFs from video files (mp4, mov, etc.).
The output will be extracted to the same folder as the input.

Example: `mpeg2gif ~/Downloads/foo.mp4` will convert `foo.mp4` to `foo.gif`.

ffmpeg is required to run this program.
If you want to pass additional options to ffmpeg, use

If you add options after the file name specification, these options will be pass ffmpeg.
```bash
mpeg2gif ~/Downloads/hoge.mp4 -r 10
```
will execute `ffmpeg -r 10 -i ~/Downloads/hoge.mp4 ....`.

#### Requirements
- ffmpeg

#### References
How to shoot video when developing smartphone apps.

## iOS
1. Connect your iPhone to your Mac
2. Open the QuickTime Player app on your Mac
3. Record a new movie -> select iPhone from the bottom center next to the ● button
4. Prepare to record on iPhone (e.g. launch the target app)
5. Press the ● button on your Mac to start recording - stop when finished
6. On your Mac, go to File → Save and save the file as any file name (hoge.mov).

## Android (Example of using ADB command) 
You can use adb_screenrecord_pull command in this repository.
Or manually, follow these steps.
1. Connect your Android device to your PC.
2. Prepare for recording on Android (e.g. launch the target app)
3. Start recording from command line as `adb shell screenrecord /sdcard/hoge.mp4` (file name is optional)
4. Press Ctrl+C on command line to finish recording
5. `adb pull /sdcard/hoge.mp4` to transfer from Android to PC
6. Delete the recording file from Android by `adb shell rm /sdcard/hoge.mp4`.


