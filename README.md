# BoringdroidSystemUI

The BoringdroidSystemUI is a pc-style SystemUI implementation that uses 
[SystemUI plugin](https://android.googlesource.com/platform/frameworks/base/+/refs/heads/master/packages/SystemUI/plugin/)
to hook itself to SystemUI.

It also uses 
[SystemUI SharedLib](https://android.googlesource.com/platform/frameworks/base/+/refs/heads/master/packages/SystemUI/shared/)
to receive the task changed events from system.

We provide gradle build script to build app with gradle, and develop it with Android Studio. It uses the keystore
generated from AOSP debug key, and it will help to install debug app from Android Studio to Android.

Both `Android.bp` and `build.gradle` use jars of above library to remove system API dependency, and
built this project directly and separately. The jars are built from system, so we should update them
when we upgrade AOSP.