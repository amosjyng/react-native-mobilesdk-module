fastlane documentation
================
# Installation

Make sure you have the latest version of the Xcode command line tools installed:

```
xcode-select --install
```

Install _fastlane_ using
```
[sudo] gem install fastlane -NV
```
or alternatively using `brew install fastlane`

# Available Actions
## Android
### android build
```
fastlane android build
```
Makes `./android/app/build/outputs/apk/release/app-release.apk` file

----

## iOS
### ios build
```
fastlane ios build
```
Makes ./ios/build/SumSubRN.ipa
### ios beta
```
fastlane ios beta
```
Updates the build number, builds then pushes .ipa to TestFlight

----

This README.md is auto-generated and will be re-generated every time [fastlane](https://fastlane.tools) is run.
More information about fastlane can be found on [fastlane.tools](https://fastlane.tools).
The documentation of fastlane can be found on [docs.fastlane.tools](https://docs.fastlane.tools).
