# Termux APK signed for Android Emacs, works on Android 15

This repo contains an Android Termux APK, that I downloaded from F-droid, and re-signed with the Android Emacs key.

I downloaded the APK 2025-08-21 around 08.00 GMT.
The version is "Version 0.119.0-beta.3 (1022) - Added on May 29, 2025".

It was downloaded from: https://f-droid.org/en/packages/com.termux/

I downloaded the signing key from here: https://github.com/emacs-mirror/emacs/tree/master/java/emacs.keystore

I used the following command to sign the APK. It was derived from https://github.com/emacs-mirror/emacs/tree/master/java/Makefile.in

apksigner sign --v2-signing-enabled --ks emacs.keystore -debuggable-apk-permitted --ks-pass pass:emacs1 com.termux_1022.apk

This APK works for me on my Android devices, that at the date of writing have the current version of Android provided by OnePlus and Samsung respectively:
- OnePlus Open
- Samsung Tab S8+

Note: If want to do your own signing, and wonder how to install the relevant signing tools, you will have to look elsewhere. I am sorry, but I do not have a pointer to a good (and up to date) instruction for how to install the relevant Android development tools.
