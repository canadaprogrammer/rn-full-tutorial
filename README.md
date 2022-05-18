# React Native Tutorial

## Methods of creating React Native app

- Expo CLI

  - Free third-party service

  - Less complicated workflow

  - Native features out-of-the-box

  - Dedicated Android and iOS app

  - Limited to the Expo ecosystem

- React Native CLI

  - React Native team & community

  - Barebone development setup

  - Configure on your own

  - Write your own native code

  - more Complicated

  - more native features

### Creating App with Expo CLI

- `expo init first-app` and choose blank

- ```bash
  cd first-app
  yarn start
  ```

### Creating App with React Native CLI for Windows and Android

- Install Chocolatey

  - `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))` on powershell

  - `choco install -y nodejs-lts openjdk11` on powershell

- It needs Node 14 or newer and JDK 11 or newer. Check the version.

  - ```
    node -v
    java -version
    ```

- Install Android Studio

- On Android Studio

  - Configure - SDK Manager

  - Select the "SDK Platforms" tab from within the SDK Manager, then check the box next to "Show Package Details" in the bottom right corner. Look for and expand the Android 11 (R) entry, then make sure the following items are checked:

    - Android SDK Platform 30
    - Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image

  - Next, select the "SDK Tools" tab and check the box next to "Show Package Details" here as well. Look for and expand the "Android SDK Build-Tools" entry, then make sure that 30.0.2 is selected.

  - Finally, click "Apply" to download and install the Android SDK and related build tools.

- Search Environment Variables on windows and click Environment Variables in System Properties

  - Click New in User variables

    - variable name: ANDROID_HOME, variable value: the path to your Android SDK

      - The SDK is installed, by default, at the following location: `%LOCALAPPDATA%\Android\Sdk`

      - You can find the actual location of the SDK in the Android Studio "Settings" dialog, under Appearance & Behavior → System Settings → Android SDK.

    - To verify `ANDROID_HOME` has been added, `Get-ChildItem -Path Env:\` on powershell

  - Double click Path in User variables

    - Click New and add the path, `%LOCALAPPDATA%\Android\Sdk\platform-tools`

- Create a new React Native project

  - `npx react-native init AwesomeProject`

- On Android Studio

  - Configure - AVD Manager - Choose Device

  - Configure - SDK Manager - Check Intel x86 Emulator Accelerator

- Run react native app

  - `cd AwesomeProject`

  - To start Metro, `npx react-native start`

  - on a new terminal, `cd AwesomeProject`

  - To start app, `npx react-native run-android`

  - `App.js` is working for the app

### eject Expo

- ```
  cd first-app
  npm run eject
  ```

  - Would you like to proceed? - yes

  - What would you like your Android package name to be? - firstapp

  - What would you like your iOS bundle identifier to be? - firstapp

- `npm react-native run-android`
