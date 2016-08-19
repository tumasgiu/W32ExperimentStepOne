
### Cygwin 2.5.2 and [swift-cygwin-20160815](https://github.com/tinysun212/swift-windows/releases/tag/swift-cygwin-20160815) (tested on Windows 10 and 7) :

Remove module cache directory before you compile (every time) :  
`rm -rf /tmp/org.llvm.clang.*`  

* `swift Hello.swift`  
Executes OK

* `swiftc Hello.swift`  
Compiles `Hello.exe` and executes OK

* `swiftc -I CWin32/ -I /usr/include/w32api/ -I /usr/include/ HelloW32.swift`  
Compiles `HelloW32.exe` and executes OK


### Windows 10 with [swift-msvc-20160515](https://github.com/tinysun212/swift-windows/releases/tag/swift-msvc-20160515)

* `swift Hello.swift`  
Executes OK

* `swiftc Hello.swift`  

No output, No .exe  

Ouput with `-v` flag  

```
Swift version 3.0-dev (LLVM f5d2d3e78d, Clang 296a35f432, Swift 5e4ad07574)
Target: x86_64-pc-windows-msvc
"c:\\Program Files\\Swift\\bin\\swiftc.exe" -frontend -c -primary-file Hello.swift -target x86_64-pc-windows-msvc -disable-objc-interop -color-diagnostics -module-name Hello -o "C:\\Users\\tumasgiu\\AppData\\Local\\Temp\\Hello-36a3b2.o"
```