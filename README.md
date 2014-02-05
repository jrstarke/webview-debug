# WebViewDebug Android Plugin for Cordova 3.2 #
By Jamie Starke

Please note that as of Cordova 3.3.0, this functionality is supported directly by Cordova, and this plugin is not required.

## Why do you want this? ##
As of Android 4.4, Google has enabled some amazing new functionality, [Debugging Android WebViews](https://developers.google.com/chrome-developer-tools/docs/remote-debugging#debugging-webviews).

To be able to enable this functionality though, you have to add a piece of code to [Configure your WebViews for Debugging](https://developers.google.com/chrome-developer-tools/docs/remote-debugging#configure-webview)

Since this was something I would need while developing, but not during production, I figured that I would make this
as a plugin, so it could easily be removed before I release my code.

## Requirements ##

You will require the Android 4.4 (SDK 19) build tools and SDK.

The `platforms/android/project.properties` file will need to be updated so that `target=android-19` as this was functionality added
in Android 4.4.

You may also have to [change your Android Target from 17 to 19](http://stackoverflow.com/a/19734065/1017797). Follow that post, but
instead of using `18` use `19`.

## Adding the Plugin to your project ##
1. To install the plugin, use the Cordova CLI and enter the following:

    cordova plugin add https://github.com/jrstarke/webview-debug.git

## Removing the plugin before you release ##
1. To remove the plugin use the Cordova CLI and enter the following:

    cordova plugin remove com.jamiestarke.webviewdebug

## To Debug WebViews ##

Make sure that you have [adb installed](https://developers.google.com/chrome-developer-tools/docs/remote-debugging#install-adbplugin),
and that [USB debugging is enabled on your device](https://developers.google.com/chrome-developer-tools/docs/remote-debugging#enable-usb-debugging).

1. Connect your device to your computer using a USB cable.
2. In your Chrome 30+ browser, open the url **about:inspect**.
3. Find the application you would like to debug in the list, and click the `inspect` link.

## Licence ##

Copyright 2013 Jamie Starke

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
