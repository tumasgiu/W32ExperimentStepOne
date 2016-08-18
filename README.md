
### Under Windows 7 x64 with Cygwin 2.5.2 and [swift-cygwin-20160815](https://github.com/tinysun212/swift-windows/releases/tag/swift-cygwin-20160815)

* `swift Hello.swift` 
Executes OK

* `swiftc Hello.swift` 
Compiles `Hello.exe` and executes OK

* `swift -I CWin32/ -I /usr/include/w32api/ -I /usr/include/ HelloW32.swift`

```
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
/home/tumasgiu/workspace/W32ExperimentStepOne/CWin32/CWin32.h:1:10: note: in file included from /home/tumasgiu/workspace/W32ExperimentStepOne/CWin32/CWin32.h:1:
#include <windows.h>
         ^
/usr/include/w32api/windows.h:97:10: note: in file included from /usr/include/w32api/windows.h:97:
#include <winscard.h>
         ^
/usr/include/w32api/winscard.h:10:10: note: in file included from /usr/include/w32api/winscard.h:10:
#include <wtypes.h>
         ^
/usr/include/w32api/wtypes.h:12:10: note: in file included from /usr/include/w32api/wtypes.h:12:
#include <ole2.h>
         ^
/usr/include/w32api/ole2.h:17:10: note: in file included from /usr/include/w32api/ole2.h:17:
#include <objbase.h>
         ^
/usr/include/w32api/objbase.h:66:10: note: in file included from /usr/include/w32api/objbase.h:66:
#include <objidl.h>
         ^
/usr/include/w32api/objidl.h:11413:20: warning: declaration does not declare anything
    __C89_NAMELESS struct _STGMEDIUM_UNION {
                   ^
LLVM ERROR: Program used external function '__imp_MessageBoxA' which could not be resolved!

```

### Under Windows 10 with Cygwin 2.5.2 and [swift-cygwin-20160815](https://github.com/tinysun212/swift-windows/releases/tag/swift-cygwin-20160815)

Exactly the same as on windows 7

### Under Windows 10 with [swift-msvc-20160515](https://github.com/tinysun212/swift-windows/releases/tag/swift-msvc-20160515)

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