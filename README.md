# jlink-jpackage-test

When properties imageName and installerName has different values, task jpackage fails to build exe installer with WiX:

```
jlink {
...
    jpackage {
...
        imageName = 'test imageName'
        installerName = 'test installerName'
```

When values are identical, build is successful, and installation and installed application works OK.

OpenJDK 15.0.1, Windows 8.1, WiX 3.11.2

'org.beryx.jlink' version '2.23.1'

https://github.com/beryx/badass-jlink-plugin/issues/169
