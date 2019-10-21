# helloworld-swift
A swift hello world project.



# Prepare

```sh
# PLEASE IGNORE THIS
if [ ! -s /usr/local/bin/swift ]; then
    ln -s /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/swift /usr/local/bin/swift
fi
```



# QuickStart

```sh
echo 'print("Hello World")' > helloworld.swift

xcrun swift helloworld.swift

# compile and run app
swiftc helloworld.swift -o helloworld
./helloworld

otool -L helloworld
helloworld:
	/System/Library/Frameworks/CoreFoundation.framework/Versions/A/CoreFoundation (compatibility version 150.0.0, current version 1349.64.0)
	/usr/lib/libobjc.A.dylib (compatibility version 1.0.0, current version 228.0.0)
	/usr/lib/libSystem.B.dylib (compatibility version 1.0.0, current version 1238.50.2)
	@rpath/libswiftCore.dylib (compatibility version 1.0.0, current version 802.0.53)
	@rpath/libswiftSwiftOnoneSupport.dylib (compatibility version 1.0.0, current version 802.0.53)
```

# Use other SDK

```sh
swiftc -sdk $(xcrun --show-sdk-path --sdk macosx) helloworld.swift
./helloworld
```

