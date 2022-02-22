# Demo App

## How to Run

1. Set up `react-native` environment following [the instructions](https://reactnative.dev/docs/environment-setup)
2. In project checkout directory, run `npm install`
3. Run demo with either `npm run ios` or `npm run android` command

## How to Upgrade

### iOS

```bash
cd ios && pod update IdensicMobileSDK && cd ..
```

## How to Distribute

### Prerequisites 

Install the [Cocoapods](https://cocoapods.org/) and [Fastlane](https://fastlane.tools/) if not yet
```sh
bundle install
```

### Prepare environment

Create `.env` file and put there the credentials as follows:
```text
APP_STORE_CONNECT_API_KEY_KEY_ID={key-id}
APP_STORE_CONNECT_API_KEY_ISSUER_ID={the-issuer-id}
APP_STORE_CONNECT_API_KEY_KEY_FILEPATH={path-to-p8-file}
```

### iOS app

The following command will set the build number according to the current number of commits, then build `./ios/build/SumSubRN.ipa` file and upload it to TestFlight.
```sh
bundle exec fastlane ios beta
```
Pay attention please that all the changes made by the command in  `./ios` dir will be stashed right after the build is done.

In case you'd like to set a specific build number for some reasons, you can run as follows:
```sh
bundle exec fastlane ios beta force_build_number:{number}
```

### Android app

The following command will produce `./android/app/build/outputs/apk/release/app-release.apk` file  
```sh
bundle exec fastlane android build
```
