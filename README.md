# Expo CI/CD for Android (continuous integration and continuous delivery/deployment)

### 1. Prepare your Expo project
Ensure your Expo project is ready for deployment.
my peoject its just a blank react native project.

### 2. Login to [expo.dev](https://expo.dev/)
Access your Expo account on [expo.dev](https://expo.dev/)

### 3. Install eas-cli

Install the EAS Command Line Interface (CLI) globally using npm:
```
npm install -g eas-cli
```
### 4. Eas login

Log in to EAS using the CLI:

```
eas login
```

Enter your Expo username and password when prompted.

### 5. Build Configure

Configure your build settings:
```
eas build:configure
```
Choose: Android

![image](https://github.com/ascaryaaa/expo-cicd/assets/73589875/d7f9870d-3023-443b-b192-d2fcc657cbd0)

### 6. Build

Initiate the build process:

```
eas build
```
- What would you like your Android application id to be? example: com.orgname.appname
- Generate a new Android Keystore: yes (Y)

### 7. Download

- Navigate to the Expo.dev overview, where you can find your project build.

![image](https://github.com/ascaryaaa/expo-cicd/assets/73589875/243bc0f1-206e-4dd1-aed1-465c9e4ffb80)

- Select your build (AAB).

![image](https://github.com/ascaryaaa/expo-cicd/assets/73589875/b7b6a203-ffec-4919-b4df-70e54d3b43b6)

- Download the build artifact.

### 8.Configuring a profile to build APKs

To configure a profile for building APKs, add the following code snippet to the `eas.json` file in your project:

```
      "android": {
        "buildType": "apk",
        "gradleCommand": ":app:assembleRelease"
      }
```

### 9. Run Build

Initiate the build process using the configured profile:

```
eas build -p android --profile preview
```

This command will execute the build process specifically for Android, utilizing the specified profile named "preview." Ensure your project settings align with this configuration before running the build command.

### 10. Install

- Navigate to the Expo.dev overview, where you can find your project build.

![image](https://github.com/ascaryaaa/expo-cicd/assets/73589875/402f05f8-a9b7-4766-a29a-a3e7a154da18)

- Select your build (APK).

![image](https://github.com/ascaryaaa/expo-cicd/assets/73589875/5dbd0a55-0033-4d6e-89b7-1d2d33886540)

- Install

You can click install or scan the bar code, then install the app and open it
Install Apk          |  Open Apk
:-------------------------:|:-------------------------:
![install](https://github.com/ascaryaaa/expo-cicd/assets/73589875/442fc96f-c2b3-478f-98a7-d7b9ffa1fe2c)  |  ![working](https://github.com/ascaryaaa/expo-cicd/assets/73589875/5a3558ac-1be5-4331-97b7-6bfbce68e746) | width=100

