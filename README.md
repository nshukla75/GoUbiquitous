# Go Ubiquitous
Project6-Udacity-GoUbiquitous
  - ABuilt a watch face for Android Wear so users can access Sunshine's weather information at a glance.
  
#Execution Instructions
Requires: Android Studio v1.5.0+, Handheld Mobile and Android Watch emulator

Dependencies:
-------------
Min SDK Version: 10 (Gingerbread 2.3.3)
Target SDK Version: 23 (Android Marshmallow)
Android Support Library v7 revision 22.1.1

Building/Running the app:
-------------------------

#### Setting up the Java Environment
Install the [Java SDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) on your system.

#### Set up Git Repository
*  Install git.  For Windows users, you may wish to do so by installing [GitHub for Windows](https://windows.github.com/).  For Mac users, there is [GitHub for Mac](https://mac.github.com/).
*  Clone the project repository.  To do so with the GitHub application, click the plus sign in the upper left, and select to clone a repository.
    -  The project repository URL to clone with public access is:
    [https://github.com/nshukla75/XYZReader.git](https://github.com/nshukla75/XYZReader.git)

#### Installing Android SDK Dependencies
*  Install [Android Studio](https://developer.android.com/sdk/installing/studio.html).
*  Launch Android Studio and select to 'Import Project' from the project directory cloned to above.
*  Then, in Android Studio, go to Tools->Android->SDK Manager and
install the following:
  -  Tools -> Android SDK Build-tools 22.1
  -  Android 5.1.1K (API V22) -> SDK Platform and Google APIs
       - For running in an emulator, install one or both system images.  The Intel x86 system image will run much faster than ARM, especially if hardware acceleration is enabled.
  -  Extras -> Android Support Library
  -  Extras -> Android Support Repository
  -  Extras -> Google Play Services (v.19)
  -  Extras -> Google Repository
  -  For a faster emulator on Windows, Extras -> Intel x86 Emulator Accelerator
  
#### Install device drivers and enable debug mode on device
*  Windows users will need to install the appropriate USB driver for their device in order to run the app on a device.  Please see the [list of available USB drivers](http://developer.android.com/tools/extras/oem-usb.html) and installation instructions.
* You can [enable debug mode on your device](http://developer.android.com/tools/device.html) to allow debugging over USB.

#### Running in an emulator
The app will run on an Android emulator.  
The emulator will run much faster with hardware acceleration enabled.  Please see the [directions on using the Android emulator and enabling hardware acceleration](http://developer.android.com/tools/devices/emulator.html).  For Windows, this uses the HAXM emulator accelerator package available under 'Extras' in the SDK Manager.

#### Running the app
To set up an Android Wear virtual device:
-  Click Tools > Android > AVD Manager.
-  Click Create Virtual Device....
-  Click Wear in the Category list:
-  Select Android Wear Square or Android Wear Round.
-  Click Next.
-  Select a release name (for example, KitKat Wear).
-  Click Next.
(Optional) Change any preferences for your virtual device.
-  Click Finish.
-  Start the emulator:
-  Select the virtual device you just created.
-  Click the Play button.
-  Wait until the emulator initializes and shows the Android Wear home screen.
-  Pair your handheld with the emulator:
-  On your handheld, install the Android Wear app from Google Play.
-  Connect the handheld to your machine through USB.
-  Forward the AVD's communication port to the connected handheld device (you must do this every time the handheld is connected):
adb -d forward tcp:5601 tcp:5601
-  Sync your gradle build file if your IDE asks you to, and then run the app via Run -> Run.
-  Start the Android Wear app on your handheld device and connect to the emulator.
-  Tap the menu on the top right corner of the Android Wear app and select sunshinewatchface card.
-  The cards you select appear as notifications on the home screen of the emulator.


Troubleshooting Steps
---------------------

If the project won't build, here are a few steps to try:

1.  Shelve any changes:  VCS -> Shelve Changes
2.  Sync the gradle files:  Tools -> Android -> Sync Project with Gradle Files
3.  Clean the project build:  Build -> Clean project


