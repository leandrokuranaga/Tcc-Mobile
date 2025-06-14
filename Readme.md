# Requirements to Test the Application

![React Native](https://img.shields.io/badge/React%20Native-20232A?style=for-the-badge\&logo=react\&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge\&logo=node.js\&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge\&logo=android-studio\&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge\&logo=java\&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge\&logo=git\&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

---

* [Install Visual Studio Code](https://code.visualstudio.com/download)
* [Install Node.js](https://nodejs.org/en/download/)
* [Install Android Studio](https://developer.android.com/studio/install?hl=en)
* [Install Java](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Install Git](https://git-scm.com/downloads)

---

## Useful Commands

To check Java version:

```bash
java -version
```

To check Node version:

```bash
node -v
```

To check npm version:

```bash
npm -v
```

---

## Add Environment Variables

1. Press `Windows + E`, right-click on **This PC**.
2. Click on **Advanced system settings**.
3. Click on **Environment Variables**.

---

## Java

To add the JAVA path:

* Go to `C:/Program Files/Java/`, open the JDK version folder, and copy the path.
* In **System Variables**, click **New**:

  * Variable Name: `JAVA_HOME`
  * Variable Value: *Paste the copied path*

---

## Android

To find the SDK path:

* Open Android Studio → Settings → SDK Manager.
* Copy the **Android SDK Location** from the top.
* In **User Variables**, create a new variable:

  * Name: `ANDROID_HOME`
  * Value: *Paste the SDK path*

Then add the following to the **Path** (User Variables):

```
%ANDROID_HOME%\emulator
%ANDROID_HOME%\tools
%ANDROID_HOME%\tools\bin
%ANDROID_HOME%\platform-tools
```

**To test in CMD:**

```bash
adb --version        # Tests %ANDROID_HOME%
emulator -version    # Tests emulator path
sdkmanager --licenses # Accept licenses (use Y)
```

---

## Emulator with CLI (Always use CMD)

```bash
emulator -list-avds
emulator -no-snapshot -avd "DeviceVersion"
npm i -g react-native-cli
mkdir "folderName"
react-native init "projectName"
cd projectName
react-native run-android
code .
```

> Start coding in `App.js`

---

## Emulator Using Physical Device (Expo)

* Install [Expo app](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=pt_BR) on your phone

```bash
npm i -g create-react-native-app
create-react-native-app "AppName"
cd AppName
code .
npm start
```

> Scan the QR Code shown to run the app. Start coding in `App.js`

---

## Emulator Using Physical Device (No Expo)

```bash
npm i -g create-react-native-app
create-react-native-app "AppName"
cd AppName
code .
# Plug your mobile device via USB
react-native run-android
```

> Start coding in `App.js`

---

## Using an Existing Project

```bash
git clone "project.git"
cd projectFolder
code .
npm install
npm run android
```

---

## Common Dev Server Errors

* Delete the `node_modules` folder:

```bash
rm -rf node_modules
```

* Reinstall packages:

```bash
npm install
```

* Run the app again:

```bash
npm run android
```
📜 License

This project is licensed under the MIT License.

