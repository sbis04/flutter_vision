# Flutter Vision

This is a Flutter app having **text recognition** functionality for detecting **email addresses** from images, built using [Firebase ML Kit](https://firebase.google.com/docs/ml-kit).

## Plugins

The plugins used in this project are:

* [camera](https://pub.dev/packages/camera)
* [firebase_ml_vision](https://pub.dev/packages/firebase_ml_vision)
* [path_provider](https://pub.dev/packages/path_provider)
* [intl](https://pub.dev/packages/intl)

## App Screenshot

<p align="center">
  <img src="https://github.com/sbis04/flutter_vision/raw/master/Screenshots/mlkit.png" alt="Flutter Vision" />
</p>

## Required configurations

Make sure you complete the following configurations before running the app on your device.

### Android

Go to **project directory** -> **android** -> **app** -> **build.gradle** and set the **minSdkVersion** to **21**:

```gradle
minSdkVersion 21
```

### iOS

* Add the following in `ios/Runner/Info.plist`:
  ```plist
  <key>NSCameraUsageDescription</key>
  <string>Can I use the camera please?</string>
  <key>NSMicrophoneUsageDescription</key>
  <string>Can I use the mic please?</string>
  ```

* Go to `ios/Podfile`.
  * Uncomment this line:
    ```Podfile
    platform :ios, '9.0'
    ```

  * Add the following at the end:
    ```Podfile
    pod 'Firebase/MLVisionBarcodeModel'
    pod 'Firebase/MLVisionFaceModel'
    pod 'Firebase/MLVisionLabelModel'
    pod 'Firebase/MLVisionTextModel'
    ```

Now, you are ready to run the app on your device.

## LICENSE

Copyright (c) 2020 Souvik Biswas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
