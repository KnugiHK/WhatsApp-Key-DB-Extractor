# WhatsApp Key/DB Extractor
Allows WhatsApp users to extract their cipher key and databases on non-rooted Android 13 or lower devices.

**Android 14 and newer ARE NOT SUPPORTED!**

> [!TIP]
> Crypt15 encrypted_backup.key is now supported!

# CAUTION (READ BEFORE PROCEED)
> [!CAUTION]
> **By default, this script use the old WhatsApp APK from WhatsApp.com (in Web Archive), use it at your own risk.**  

> [!IMPORTANT]
> Always create a backup through the official WhatsApp app if possible before trying or you risk losing all your data...

## APK Integrity
Checksum are as follows:
* 51a387f08debd7e53bcaf9f3174760930787bc5c1dcefb3c8d7ee52b524cd27d  WhatsApp.apk (2.11.431)

Source:
* WhatsApp.apk: https://web.archive.org/web/20141111030303/http://www.whatsapp.com/android/current/WhatsApp.apk


## BRANCH UPDATES
v4.0 - Fixed issues with Android API 14-17 (4.0-4.2 Jelly Bean).  
v4.1 - Added support for Android API 23 (6.0-6.0.1 Marshmallow).  
v4.2 - Added support for specifying adb backup passwords.  
v4.3 - Added PowerShell version as optional alternative to bat version.  
v4.4 - Changed primary mirror for legacy apk.  
v4.5 - Fixed issue pushing cipher key to emulated storage.  
v4.6 - Updated primary mirror for legacy apk (again).  
v4.7 - Added new sanity checks and support for Android API 24 (7.0 Nougat).  
v5.0 - Fixed the link of legacy apk.  
v5.1 - Added support for Crypt15.  
v5.2 - Fixed the link of legacy apk.  
v5.3 - Added a pause for users accepting the permissions request.  
v5.4 - Updated the binaries for ABE and CURL.  
v5.5 - Updated binaries and drop support for bat version


## PREREQUISITES:
 1. O/S: Windows 10, Windows 11, Mac OS X or Linux  
 2. Java - If not installed: https://www.java.com/en/download/  
 3. ADB (Android Debug Bridge) Drivers: https://developer.android.com/tools/releases/platform-tools
 4. USB Debugging must be enabled on the target device. Settings -> Developer Options -> (Debugging) USB debugging  
     If you cannot find Developer Options then please go to: Settings -> About phone/device and tap the Build number  
     multiple times until you're finally declared a developer.  
 5. Android device running version 4.0 to 13.


## INSTRUCTIONS:
 1. Extract "WhatsApp-Key-DB-Extractor-master.zip" maintaining the directory structure.  
 2. Click on "WhatsAppKeyDBExtract.ps1" (Windows) or "WhatsAppKeyDBExtract.sh" (Mac OS X / Linux).  
 3. Connect your device via USB, unlock your screen and wait for "Full backup" or the permission request screen to appear.  
 4. Enter your backup password or leave blank (if none set) and tap on "Back up my data".  
 5. Confirm backup password in your command console and then check your "extracted" folder.  
 

## TROUBLESHOOTING:
 1. If you have never used USB Debugging before, you may also need to verify the fingerprint.  
 2. If you have set a default backup password in your Android settings, then this MUST be the  
     backup password that you PROVIDE when prompted to backup your data. Else it WILL fail!  
 3. Linux and Mac OS X users may need to set the script permissions as executable. Depending on the  
     adb permissions, you may also need to "sudo ./WhatsAppKeyDBExtract.sh" from your command console.  
 4. If you get an error saying "AES encryption not allowed" then you need to update your Oracle Java  
    Cryptography Extension (JCE) to Unlimited Strength Jurisdiction Policy Files.  


## CREDITS:
AUTHOR: TripCode  
MAINTAINER: KnugiHK  
THANKS: dragomerlin for Android Backup Extractor and Abinash Bishoyi for being cool.  
abe.jar by nelenkov and its contributors.  
tar.exe, grep.exe, regex2.dll, libintl3.dll, libiconv2.dll by Free Software Foundation and its contributors.  
pcre3.dll by University of Cambridge and its contributors.  
curl.exe by Daniel Stenberg and its contributors.  
adb.exe, AdbWinApi.dll, AdbWinUsbApi.dll by The Android Open Source Project and its contributors.  
`SPDX-License-Identifier: Apache-2.0 OR GPL-3.0`
