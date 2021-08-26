Flutter VS Code Only for Windows 10

```
`No suitable Android AVD system images are available. You may need to install these using sdkmanager, for example: sdkmanager "system-images;android-27;google_apis_playstore;x86".'
```

```
flutter config --machine
sdkmanager "system-images;android-27;google_apis_playstore;x86"
```

*If*
```
sdkmanager : The term 'sdkmanager' is not recognized as the name of a cmdlet, function, script file, or operable program.
```
*Then* Changed PATH variable to point towards: %USERPROFILE%\AppData\Local\Android\Sdk\tools\bin

*If*
```
Exception in thread "main" java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema
        at com.android.repository.api.SchemaModule$SchemaModuleVersion.<init>(SchemaModule.java:156)
        at com.android.repository.api.SchemaModule.<init>(SchemaModule.java:75)
        at com.android.sdklib.repository.AndroidSdkHandler.<clinit>(AndroidSdkHandler.java:81)
        at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:73)
        at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:48)
Caused by: java.lang.ClassNotFoundException: javax.xml.bind.annotation.XmlSchema
        at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:636)
        at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:182)
        at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:519)
        ... 5 more
```

*Then*

```
choco install jdk8
sdkmanager --update
sdkmanager "system-images;android-27;google_apis_playstore;x86"
```
