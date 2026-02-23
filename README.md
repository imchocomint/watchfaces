# Watchfaces (for Android 13+ (WearOS 4))
WearOS watchfaces. Created by me in Samsung's Watch Face Studio.

[Art credits](https://github.com/imchocomint/watchfaces/blob/main/credits.md)

## Download and install
Grab the files in Release (apk)

[Pair the watch with your computer's adb](https://developer.android.com/training/wearables/get-started/debugging#physical-watch). Install like any normal app:

` adb install [filename] `

Long press your homescreen, then scroll to the rightmost tab (plus sign). Scroll to the bottom and choose watchfaces to set.

## Compile
Compile via [Watch Face Studio](https://developer.samsung.com/watch-face-studio/download.html)
### Generate a keystore
Install JDK (whatever is fine, but preferably 17+). Navigate to your install directory

Run: ` keytool -genkeypair -v -storetype PKCS12 -keystore upload-key.keystore -alias watch -keyalg RSA -keysize 2048 -validity 10000 `. Input everything it requires.

### Compile
Open the wfs files in Watch Face Studio. Click 'Publish' (top right, next to 'Run on Device').

Name your package, and change the version if needed. Change publish type to APK. Change the keystore path to the file you generated in the previous step. Use the same passwords you entered while generating the keystore for both fields. Change app label if needed. Press OK and wait.

## Device support
### Tier 1
Galaxy Watch 4/5 40mm, Galaxy Watch 4 Classic, Galaxy Watch FE

### Tier 2 
Any other WearOS devices. May have tearing on larger watches.
