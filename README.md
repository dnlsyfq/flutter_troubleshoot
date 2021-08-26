Flutter VS Code Only for Windows 10

```
`No suitable Android AVD system images are available. You may need to install these using sdkmanager, for example: sdkmanager "system-images;android-27;google_apis_playstore;x86".'
```

```
flutter config --machine
sdkmanager "system-images;android-27;google_apis_playstore;x86"
```

**If**
```
sdkmanager : The term 'sdkmanager' is not recognized as the name of a cmdlet, function, script file, or operable program.
```
> Changed PATH variable to point towards: %USERPROFILE%\AppData\Local\Android\Sdk\tools\bin
