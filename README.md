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

