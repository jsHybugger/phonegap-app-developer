# PhoneGap Developer App (1.1.0) + jsHybugger (4.5.6)

## Overview

The PhoneGap Developer app is a testing utility for web developers and designers
using the PhoneGap framework. After installing the PhoneGap Developer app you
can connect to your PhoneGap desktop app to instantly view and test your project
on the device.

To debug/inspect your application just open the following url in your chrome browser: chrome://inspect

For more information, see [app.phonegap.com][3].

## Download

- http://www.jshybugger.com/examples/phonegap-app/PhoneGap-1.1.0_jsHybugger-4.5.6.apk

## Development

### Compile and Run the Application


    $ npm install
    $ npm install -g phonegap
    $ phonegap run ios
    $ phonegap run android
    $ phonegap run wp8

For developers wishing to use the platform SDKs (Xcode, Eclipse, Visual Studio),
please build once with the CLI to correctly populate the platform assets:

    $ phonegap build <platform>

### Running the Tests

There are two types of test targets: the local app and served app.

#### Test the Local Application

The local application is the PhoneGap Developer App. To test the local
functionality, we build the application with mobile-spec. This allows us to
ensure that each plugin was correctly installed. Eventually, we would like
to add functional tests for the app logic.

You can run the local tests with:

    $ phonegap run android --test
    $ phonegap run ios --test
    $ phonegap run wp8 --test

#### Test the Served Application

The served application is the app served by the CLI. To test the server
functionality, we serve an instance of mobile-spec. We can then use the manual
and automatic tests to ensure that the server provided the correct version of
Cordova, the plugins, and the navigation logic.

You can run the served tests with:

    $ cd tests/
    $ phonegap serve
    # now connect with the latest build of the PG App

### Updating the Tests

It's as easy as a copy and paste.

1. Copy all content of `cordova-mobile-spec`
2. Paste the content into `tests/www`

On your first run of the tests, you may see some modified files. This is expected
because the test runner invoked by `--test` modifies certain files to support
our app's configuration.

### Commits, Tags, and Releases

See the [CONTRIBUTING.md][6] file for details.

[1]: https://play.google.com/store/apps/details?id=com.adobe.phonegap.app
[2]: https://itunes.apple.com/app/id843536693
[3]: http://app.phonegap.com
[4]: http://github.com/phonegap/connect-phonegap
[5]: http://github.com/phonegap/phonegap-cli
[6]: https://github.com/phonegap/phonegap-app-developer/blob/master/CONTRIBUTING.md
[7]: http://www.windowsphone.com/en-us/store/app/phonegap-developer/5c6a2d1e-4fad-4bf8-aaf7-71380cc84fe3

