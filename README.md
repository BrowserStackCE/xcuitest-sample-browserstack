# XCUITests with A11yUITests for Accessibility Testing on iOS devices

A sample iOS app supporting [XCUI Tests](https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/testing_with_xcode/chapters/09-ui_testing.html) on [Browserstack](https://www.browserstack.com/).

<img src="https://cdn-images-1.medium.com/max/1600/1*Z0AH-kvjNsUKlcgjP01rmA.png" height="120" /> ![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Pre-requisites

1. XCode ( Download it from [here](https://developer.apple.com/xcode/resources/) )
2. CocoPods ( Download it from [here](https://guides.cocoapods.org/using/getting-started.html) )

<b>Note:</b> Developer Certificate would be required to build the iOS App.

Once the above steps are in place. Execute the below command.
```
pod install
```

## Running tests on BrowserStack App-Automate

1. Select the device as "Generic iOS device"
2. Product -> Clean Build
3. Product -> Clean Test
4. Build the ipa
	1. Product -> Archive
	2. Window -> Organizer -> Select the most recently created archive -> Export
	3. Export for "Development"
	4. Select the location where you want the ipa to be saved
5. Build the XC UI Tests zip
	1. Product -> Build For -> Testing
	2. From the shell, go to the DerivedData directory (normally ~/Library/Developer/Xcode/DerivedData/)
	3. cd Sample_iOS-&lt;random characters&gt;
	4. cd Build/Products/Debug-iphoneos/
	5. zip -r SampleUITests.zip SampleXCUITests-Runner.app/

6. Use the ipa file and zip file you have created using the above steps to run on Browserstack

## Note : 
* Follow [This](https://www.browserstack.com/docs/app-automate/xcuitest/getting-started) for executing the tests on BrowserStack
* There are multiple tests that you can use from A11yUItests used in the `SampleXCUITests/SampleXCUITests.swift` file. Please refer to [this](https://github.com/rwapp/A11yUITests#tests) for the range of tests you can choose from.

## Links & Resources

To learn more about accessibility testing, visit the accessibility testing page on [Accessibility on iOS - Apple Developer](https://developer.apple.com/accessibility/ios/).

Get the source for the A11yUITests by visiting its [GitHub](https://github.com/rwapp/A11yUITests) repository.

Documents for reference: 
* https://mobilea11y.com/blog/a11yuitests/
* https://developer.apple.com/documentation/xctest

