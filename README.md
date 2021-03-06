# AccessoryKit

A customizable, expandable, and easy-to-use input accessory view component for iOS.

[![Version](https://img.shields.io/cocoapods/v/AccessoryKit.svg?style=flat)](https://cocoapods.org/pods/AccessoryKit)
[![License](https://img.shields.io/cocoapods/l/AccessoryKit.svg?style=flat)](https://cocoapods.org/pods/AccessoryKit)
[![Platform](https://img.shields.io/cocoapods/p/AccessoryKit.svg?style=flat)](https://cocoapods.org/pods/AccessoryKit)

## Features

**AccessoryKit** aims to provide a customizable, expandable and easy-to-use input accessory view. This component is developed for and is currently used in my app [MDNotes](https://apps.apple.com/us/app/mdnotes/id1471287219).

![](Screenshots/1.png)

The main features are:

* Scrollable input accessory view with blurry background and customizable buttons.
* Supports Auto Layout and Safe Area.
* Supports dark mode.

## Usage

### Requirements

* iOS 10.0+
* Swift 5.0+

### Installation

To install AccessoryKit, simply add the following line to your Podfile:

```ruby
pod 'AccessoryKit'
```

### Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

### API

```swift
// Create view model array of key buttons
let keyButtons: [KeyboardAccessoryButton] = [
    KeyboardAccessoryButton(type: .undo, tapHandler: { [weak self] in
        self?.undo()
    }),
    KeyboardAccessoryButton(image: UIImage(named: "img", tapHandler: {}),
]

// Initialize `KeyboardAccessoryView`
let accessoryView = KeyboardAccessoryView(
    frame: CGRect(x: 0, y: 0, width: view.frame.width, height: 0),
    keyButtons: keyButtons,
    showDismissKeyboardKey: true,
    delegate: self)

// Assign the accessory view instance to `UITextView`
textView.inputAccessoryView = accessoryView
```

## TODO

- [ ] Swift Package Manager
- [ ] Tint color
- [ ] Tweak UI

## License

AccessoryKit is available under the MIT license. See the [LICENSE](LICENSE) file for more info.
