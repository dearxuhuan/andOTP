#  andOTP -  Android OTP Authenticator

[![Build Status](https://travis-ci.org/flocke/andOTP.svg?branch=master)](https://travis-ci.org/flocke/andOTP)
[![Current release](https://img.shields.io/github/release/flocke/andOTP/all.svg)](https://github.com/flocke/andOTP/releases/download/v0.2.2/andOTP_v0.2.2.apk)

![andOTP](./assets/logo.png)

andOTP is a two-factor authentication App for Android 4.4+.

It implements Time-based One-time Passwords (TOTP) like specified in RFC 6238.  
Simply scan the QR code and login with the generated 6-digit code. 

This is a fork of the great OTP Authenticator app written by Bruno Bierbaumer,
which has sadly been inactive since 2015. All credit for the original version
goes to Bruno.

## Features:

 * Free and Open-Source
 * Requires minimal permissions
   - Camera access for QR code scanning
   - Storage access for import and export of the database
 * Encrypted storage
 * Plain-text backups
 * Encrypted backups using OpenPGP
 * Sleek minimalistic Material Design
 * Great Usability
 * Compatible with Google Authenticator

## Backups:

To keep your account information as secure as possible andOTP only stores it in
encrypted data files. A part of the encryption key used for that is stored in the
Android KeyStore system. The advantage of this approach is that the key is kept
separate from the apps data and, as a bonus, can be backed by hardware cryptography
(if your device supports this).

However, due to that separation, backups with 3rd-party apps like Titanium Backup can not
be used with andOTP. Such apps only backup the encrypted data files and not the encryption
key, which renders them useless.

**Please only use the internal backup functions provided by andOTP to backup your accounts!**
**Everything else WILL result in data loss.**

## TODO:

 * HOTP Support

## Downloads:

#### Google Play:

<a href="https://play.google.com/store/apps/details?id=org.shadowice.flocke.andotp"><img width=250 alt="Get in on Google Play" src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" /></a>

#### APKs:

 * [GitHub](https://github.com/flocke/andOTP/releases)

**Warning**: The APKs and the Play Store version are not compatible (not signed by the same key)!
You will have to uninstall one to install the other, which will delete all your data.
So make sure you have a **current backup** before switching!

## Discussion:

If you want to discuss this app, share ideas for features or get help with bugs please head over to the [XDA thread](https://forum.xda-developers.com/android/apps-games/app-andotp-android-otp-authenticator-t3636993).

## Acknowledgments:
#### Open-source components used:

 * [Apache Commons Codec](https://commons.apache.org/proper/commons-codec/)
 * [LicensesDialog](https://github.com/PSDev/LicensesDialog)
 * [MaterialProgressBar](https://github.com/DreaminginCodeZH/MaterialProgressBar)
 * [OpenPGP API library](https://github.com/open-keychain/openpgp-api)
 * [ZXing Android Embedded](https://github.com/journeyapps/zxing-android-embedded)

#### Code examples used:

 * [Android-ItemTouchHelper-Demo](https://github.com/iPaulPro/Android-ItemTouchHelper-Demo/tree/master/app/src/main/java/co/paulburke/android/itemtouchhelperdemo/helper)
 * [Code Parts from Google's Android Samples](https://android.googlesource.com/platform/development/+/master/samples/Vault/src/com/example/android/vault)
 * [FloatingActionMenuAndroid](https://github.com/pmahsky/FloatingActionMenuAndroid)

## License:
```
Copyright (C) 2017 Jakob Nixdorf <flocke@shadowice.org>
Copyright (C) 2015 Bruno Bierbaumer

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in the
Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE
OR OTHER DEALINGS IN THE SOFTWARE.
```
