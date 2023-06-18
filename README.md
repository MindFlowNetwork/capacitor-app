## Cordova Replacement: Capacitor

This app was created using [`@capacitor/create-app`](https://github.com/ionic-team/create-capacitor-app),
and explores the power of using HTML to build fast and fully functional apps that tap native capabilities when it makes sense.

## Creating from Scratch
Install node (and brew if you're on a Mac).

Now let's build the capacitor app:
```bash
npm init @capacitor/app capacitor-app --name capApp --app-id network.mindflow.captest
```

Now copy over the *src* contents to it.

Now we want to build the optimized html:
```bash
npm run build
```

Now we want to build out iOS scaffolding:
```bash
npx cap add ios
```

The first time, we open it directly in XCode to set up the signing stuff - open ios/App/App.xcworkspace.

```bash
npx cap run ios
```

Now we want to add the various permissions to allow the camera to operate so edit the *ios/App/App/Info.plist* file and add this inside the:
```xml
        <key>NSPhotoLibraryUsageDescription</key>
        <string>Camera will be used for testing.</string>
        <key>NSPhotoLibraryAddUsageDescription</key>
        <string>Camera will be used for testing.</string>
        <key>NSCameraUsageDescription</key>
        <string>Camera will be used for testing.</string>
```
Or you can run these lines together like this:

```bash
npm run build && npx cap run ios
```
