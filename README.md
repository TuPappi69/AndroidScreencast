AndroidScreencast
=================

[![Join the chat at https://gitter.im/AndroidScreencast/Lobby](https://badges.gitter.im/AndroidScreencast/Lobby.svg)](https://gitter.im/AndroidScreencast/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)



[![Build Status Travis-CI][travis_badge]][travis] [![Dependency Status][versioneye_badge]][versioneye] [![Codacy Badge][codacy_badge]][codacy]

[travis_badge]: https://travis-ci.org/xSAVIKx/AndroidScreencast.svg?branch=master
[travis]: https://travis-ci.org/xSAVIKx/AndroidScreencast

[versioneye_badge]: https://www.versioneye.com/user/projects/588988221618a700318eafb5/badge.svg
[versioneye]: https://www.versioneye.com/user/projects/588988221618a700318eafb5

[codacy_badge]: https://api.codacy.com/project/badge/Grade/064bbd2582b544bb9659a01a2872317c
[codacy]: https://www.codacy.com/app/xSAVIKx/AndroidScreencast?utm_source=github.com&utm_medium=referral&utm_content=xSAVIKx/AndroidScreencast&utm_campaign=badger

# Description

AndroidScreencast was developed to view and control your android device from a PC.

This project gives the opportunity to use your phone even with a broken screen.

## Features

- No client needed
- Support for Tap and Swipe gestures
- Write messages using PC keyboard
- Support for landscape mode
- Browse your phone files on PC
- Record video of your phone screen while browsing

[Small wiki of project][wiki]

[wiki]: https://github.com/xSAVIKx/AndroidScreencast/wiki

## JNLP

Application is available using Java web start technology via [androidscreencast.jnlp][jnlp].

[jnlp]: http://xsavikx.github.io/AndroidScreencast/jnlp/androidscreencast.jnlp

### Java security configuration

Due to Java security restriction policy, that was updated in java 7 and is restricted even more in java 8, we're now not
able to run JNLP without some security "hacks".

To use JNLP, please follow this article: [How can I configure the Exception Site List?][exception]

[exception]: https://www.java.com/en/download/faq/exception_sitelist.xml

## Building and running from source

This project requires at least Java 8.

After cloning the project, run `mvnw install`.

The resulting artifacts will be created in the `target` subdirectory.

You can run the executable jar via `java -jar target/androidscreencast-VERSION-executable.jar`, replacing VERSION with
the current version.

For example, `java -jar target/androidscreencast-0.0.8s-executable.jar`.

Additionally OS-packages would be created with ADB executables bundled:
* `androidscreencast-VERSION-windows.zip`
* `androidscreencast-VERSION-linux.tar.gz`
* `androidscreencast-VERSION-macosx.tar.gz`

# Requirements

Currently AndroidScreencast works directly with `adb input` program through `ddmlib` and abuse functionality of:
* `adb input key`
* `adb input tap`
* `adb input swipe`

Regarding this point, to use AndroidScreencast you need Smartphone running on Android with specific `input` program version. `adb input tap` and `adb input swipe` were introduced in [Android 4.1.1][Android_4_1_1_Input].

So, right now AndroidScreencast support all Android versions equal or greater than Android 4.1.1.

Also, to run AndroidScreencast you will need *adb* installed (or you can use bundled in OS bundles adb).

[Android_4_1_1_Input]: http://grepcode.com/file/repository.grepcode.com/java/ext/com.google.android/android/4.1.1_r1/com/android/commands/input/Input.java#Input
