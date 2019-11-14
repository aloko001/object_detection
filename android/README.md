# TensorFlow Lite Object Detection For Android
### Introduction
A camera app that continuously detects the objects (bounding boxes and labels) in the frames seen by your android camera, using a quantized [MobileNet SSD](https://github.com/aloko001/object_detection) model trained with tensorflow api on the [COCO dataset](http://cocodataset.org/). 
The following instructions walk you through building and running the app on an Android device.

The model files are downloaded via Gradle scripts when you build and run. You don't need to download TFLite models.

Application can run either on device or emulator.


## Build the app using Android Studio

### Dependencies 

* If you don't have the app, install **[Android Studio](https://developer.android.com/studio/index.html)**, following the instructions.

* Upgrade your Android device and Android development environment to a minimum API 21.
* Android Studio 3.2 or later is accepted.

### Compile Source Files
* Run Android Studio, and from the Welcome screen, select Open an existing Android Studio project.

* From the Open File or Project window that appears, locate and select the aloko001/object_detection/android directory from wherever you cloned the TensorFlow Lite sample GitHub repo. Click OK.

* If it asks you to do update Gradle Sync, click OK.

* You may also need to install and upgrade various platforms and tools, if you get errors like "Failed to find target with hash string 'android-21'" and similar.
Click the Run button (the green arrow) or select Run > Run 'android' from the top menu. You may need to rebuild the project using Build > Rebuild Project.

* You need to have an Android device plugged in with developer options enabled at this point. See **[here](https://developer.android.com/studio/run/device)** for more details on setting up developer devices on your device.


### Additional Note
_Do not delete the assets folder content_. If you explicitly deleted the files, then please choose *Build*->*Rebuild* from menu to re-download the deleted model files into assets folder.

### Images Generated

![Image one](https://github.com/aloko001/object_detection/blob/master/android/images_shot/android.jpg)
