PinDialog
=========

PhoneGap numeric text dialog plugin for Android and iOS. Forked from https://github.com/apache/cordova-plugin-dialogs.git

## Installation

Current state from git: ```cordova plugin add https://github.com/sjregan/PinDialog.git```

## Installation - PhoneGap Build 

Add following to config.xml: ```<gap:plugin name="sjregan.phonegap.plugins.pindialog" />```
or ```<gap:plugin name="sjregan.phonegap.plugins.pindialog" source="plugins.cordova.io" />```

## Supported Platforms

- Android
- iOS

## Usage:

    // Show pin dialog
    window.plugins.pinDialog.prompt("message", callback, "title", ["OK","Cancel"]);

Callback:

    function callback(results)
    {
        if(results.buttonIndex == 1)
        {
            // OK clicked, show input value
            alert(results.input1);
        }
        if(results.buttonIndex == 2)
        {
            // Cancel clicked
            alert("Cancel");
        }
    };
