This is a set of project files to make it possible to use OpenFrameworks with Android Studio.

# Installation

1. Install and configure Android Studio
2. Install the Android NDK somewhere
3. Download and unpack OpenFrameworks
4. Copy the files from this repository over top of the OpenFrameworks files, merging directories
    (i.e. replace existing files, but do not replace entire directories)
5. Open this directory as a project in Android Studio (use File->Open and select this directory)
6. Set `ndk.dir` in the `local.properties` to the full path to your Android NDK
7. Build and run the example app

# Usage

To create new projects, just copy the provided example app.

# Troubleshooting

- You may need to adjust the following numbers to match your installed Android Studio and Android SDK.
Android Studio should offer to fix these values for you when you open the appropriate build files.

    - The Gradle version specified in `/build.gradle`
    - The `compileSdkVersion`, `buildToolsVersion`, `minSdkVersion`, `targetSdkVersion` values
        in `/addons/ofxAndroid/ofAndroidLib/build.gradle` and `/apps/myApps/androidEmptyExample/build.gradle`

- If you get strange linker errors (e.g. errors about a missing `__srget`), try using the r9d version
of the NDK. Newer NDKs (particularly r10c and up) don't work with some versions of OpenFrameworks.

