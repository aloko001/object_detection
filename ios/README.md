# TensorFlow Lite Object Detection iOS Example Application

**iOS Versions Supported:** iOS 12.0 and above.
**Xcode Version Required:** 10.0 and above

## Introduction

A camera app that continuously detects the objects (bounding boxes and labels) in the frames seen by your iOS camera, using a quantized [MobileNet SSD](https://github.com/aloko001/object_detection) model trained on the [COCO dataset](http://cocodataset.org/). These instructions walk you through building and running the app on an iOS device.

The model files automatically downloads via scripts in Xcode when you build and run. You don't need to do any steps to download TFLite models into the projec.

<!-- TODO(b/124116863): Add app screenshot. -->

## Dependencies 

* You must have Xcode installed on your MacOS

* You must have a valid Apple Developer ID

* The demo app requires a camera and must be executed on a real iOS device.
* You don't need to build the entire TensorFlow library to run the demo, it uses CocoaPods to download the TensorFlow Lite library.

* You'll also need the Xcode command-line tools:
 ```xcode-select --install```
 If this is a new install, you will need to run the Xcode application once to agree to the license before continuing.
 
## Building the iOS Demo App

1. Install CocoaPods if you don't have it.
```sudo gem install cocoapods```

2. Install the pod to generate the workspace file:
```cd lite/examples/object_detection/ios/```
```pod install```
  If you have installed this pod before and that command doesn't work, try
```pod update```
At the end of this step you should have a file called ```ObjectDetection.xcworkspace```

3. Open **ObjectDetection.xcworkspace** in Xcode.

4. Change the iOS bundle identifier to a unique identifier and select your development team in **'General->Signing'** before building the application if you are using an iOS device.

5. Build and run the app in Xcode.
You'll have to grant permissions for the app to use the device's camera. Point the camera at various objects and enjoy seeing how the model classifies things!

### Additional Note
_Please do not delete the empty references_ to the .tflite and .txt files after you clone the repo and open the project. These references will be fulfilled once the model and label files are downloaded when the application is built and run for the first time. If you delete the references to them, you can still find that the .tflite and .txt files are downloaded to the Model folder, the next time you build the application. You will have to add the references to these files in the bundle separately in that case.
