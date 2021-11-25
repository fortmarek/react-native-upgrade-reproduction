# Reproduction of `RCT-Folly` issue when upgrading React Native

This repo serves as a reproduction example of the `RCT-Folly` issue. To reproduce the issue, change `react-native` version in `package.json` to `0.66.3`, run `yarn install` and then `cd ios && pod install`.

`pod install` should fail for you with the following:
```
[!] CocoaPods could not find compatible versions for pod "RCT-Folly":
  In snapshot (Podfile.lock):
    RCT-Folly (from `../node_modules/react-native/third-party-podspecs/RCT-Folly.podspec`)

  In Podfile:
    RCT-Folly (from `../node_modules/react-native/third-party-podspecs/RCT-Folly.podspec`)

    React-RCTNetwork (from `../node_modules/react-native/Libraries/Network`) was resolved to 0.66.3, which depends on
      RCT-Folly (= 2021.06.28.00-v2)
```