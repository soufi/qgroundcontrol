Hi! Here are two resources I found helpful:
https://dev.qgroundcontrol.com/master/en/getting_started/
https://doc.qt.io/qt-5/ios.html

This is the basic process:

Install Qt 5.12.6 and include iOS/macOS and Qt Charts in your installation
Install gstreamer if you want it
Clone QGC and updating submodules
Run qmake to build the .xcodeproj (for example: ~/Qt/5.12.6/iOS/bin/qmake /path/to/qgroundcontrol.pro CONFIG+=WarningsAsErrorsOn)
Open .xcodeproj in Xcode
Enter developer credentials
Build with Xcode's interface



```
qmake -spec macx-xcode ../qgroundcontrol.pro CONFIG+=WarningsAsErrorsOn LIBS+=-L/Library/Frameworks/GStreamer.framework/Libraries
```


```
LIBS += -L/Library/Frameworks/GStreamer.framework/Libraries
```

Super important : 

One workaround is to go into the "Signing&Capabilities" tab of your compilation target and make sure "Disable Library Validaton" is checked (this worked for me).