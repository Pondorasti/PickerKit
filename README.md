# PickerKit

<p align="center">
   <a href="https://developer.apple.com/swift/">
      <img src="https://img.shields.io/badge/Swift-5.0-orange.svg?style=flat" alt="Swift 5.0">
   </a>
   <a href="https://travis-ci.com/Pondorasti/PickerKit">
      <img src="https://travis-ci.com/Pondorasti/PickerKit.svg?branch=master" alt="CI Status">
   </a>   
   <a href="http://cocoapods.org/pods/PickerKit">
      <img src="https://img.shields.io/cocoapods/v/PickerKit.svg?style=flat" alt="Version">
   </a>
   <a href="http://cocoapods.org/pods/PickerKit">
      <img src="https://img.shields.io/cocoapods/p/PickerKit.svg?style=flat" alt="Platform">
   </a>
   <a href="https://github.com/Carthage/Carthage">
      <img src="https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat" alt="Carthage Compatible">
   </a>
   <a href="https://github.com/apple/swift-package-manager">
      <img src="https://img.shields.io/badge/Swift%20Package%20Manager-compatible-brightgreen.svg" alt="SPM">
   </a>
</p>

PickerKit is an iOS framework that streamlines the stock UIPicker into a gesture based UI with a minimalistic look, allowing to effortlessly pick something from a pool of entries(right now it only has support for colors).

<p align="center">
   <image src="https://github.com/Pondorasti/PickerKit/blob/master/Assets/PickerKit%20Preview%20GIF.gif">
</p>
   
## Features

- [x] Entries automatically resize based on height of the container (PickerView)
- [x] IBInspectable properties
- [x] Easy to set-up and customize for your own needs
- [ ] Entries Collection View Cell based on Generics for ease of customisation

## Requirements

- Xcode 10 and later
- iOS 10 and later
- Swift 5 and later

## Example

The example application is the best way to see `PickerKit` in action. Simply open the `PickerKit.xcodeproj` and run the `Example` scheme.

## Installation

### CocoaPods

PickerKit is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```bash
pod 'PickerKit'
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that builds your dependencies and provides you with binary frameworks.

To integrate PickerKit into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "Alexandru Turcanu/PickerKit"
```

Run `carthage update` to build the framework and drag the built `PickerKit.framework` into your Xcode project. 

On your application targets’ “Build Phases” settings tab, click the “+” icon and choose “New Run Script Phase” and add the Framework path as mentioned in [Carthage Getting started Step 4, 5 and 6](https://github.com/Carthage/Carthage/blob/master/README.md#if-youre-building-for-ios-tvos-or-watchos)

### Swift Package Manager

To integrate using Apple's [Swift Package Manager](https://swift.org/package-manager/), add the following as a dependency to your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/Pondorasti/PickerKit.git", from: "1.0.0")
]
```

### Manually

If you prefer not to use any of the aforementioned dependency managers, you can integrate PickerKit into your project manually. Simply drag the `Sources` Folder into your Xcode project.

## Usage

### Creating a PickerView

Creating a PickerView is as easy as just giving an array of UIColors. The view's contents, color entries, will resize accordingly to the PickerView's height. This view needs to infer it's height and width from the parent in order to work properly.

~~~swift
let colorPickerView = PickerView(
   colorEntries: [UIColor.red, UIColor.blue, UIColor.purple, UIColor.orange, UIColor.green]
)
~~~

Retrieving the selected color, this value is accesible in the selectedEntry property. Setting this value to a index in range of the colors array will automatically animate and scroll to that index.

~~~swift
colorPickerView.selectedEntry = 2
~~~

### Customizing the Appearance

A Boolean value that controls whether the fade out gradient is visible. Default value is true.

~~~swift
colorPickerView.shouldFadeOutView = true
~~~

A floating-point value that determines the radius difference between the entry item and the focus ring. Default value is 10.
    
~~~swift
colorPickerView.focusRingRadiusDelta = 10
~~~

A floating-point value that determines the spacing between each entry view. Default value is 12.
    
~~~swift
colorPickerView.lineSpacing = 12
~~~

<p align="center">
   <image src="http://giphygifs.s3.amazonaws.com/media/2YegpyGZpGnKWwWzEE/giphy.gif">
</p>

### Notes

At the moment the framework does not support high customizability nor deep access control over it, but any feature request is kindly appreciated.

## Contributing
Thank you for your interest in the project! Contributions are very welcome 🙌, feel free to collaborate with ideas 💭, issues ⁉️ and/or pull requests 🔃.

Make sure to read these guides before getting started:

- [Code of Conduct](https://github.com/Pondorasti/PickerKit/wiki/Code-of-Conduct)
- [Contribution Guidelines](https://github.com/Pondorasti/PickerKit/wiki/Contribution-Guidelines)

If you use PickerKit in your app I'd love to hear about it and feature your app here!

## Author

Written by Alexandru Turcanu


[![Twitter Follow](https://img.shields.io/twitter/follow/pondorasti.svg?style=social)](https://twitter.com/pondorasti)

[![Twitter Follow](https://img.shields.io/github/followers/pondorasti.svg?style=social&label=Follow)](https://github.com/pondorasti)


## License

PickerKit is available under the MIT license. See the [LICENSE](https://github.com/Pondorasti/PickerKit/blob/master/LICENSE) file for more info.
