
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

* `swift -I "C:\Program Files (x86)\Windows Kits\8.1\Include\um" -I CWin32 HelloW32.swift`  

```
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2809:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL                = 0x80000000,
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2810:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_OUTPUT_TECHNOLOGY_FORCE_UINT32            = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2820:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32                = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2864:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_SCALING_FORCE_UINT32              = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2873:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_ROTATION_FORCE_UINT32 = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2880:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_MODE_INFO_TYPE_FORCE_UINT32 = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2890:5: warning: enumerator value is not representable in the underlying type 'int'
    DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32  = 0xffffffff
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2976:7: warning: enumerator value is not representable in the underlying type 'int'
      DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32   = 0xFFFFFFFF
      ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:166:
#include <wingdi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\wingdi.h:2988:7: warning: enumerator value is not representable in the underlying type 'int'
      DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32                = 0xFFFFFFFF
      ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:1089:5: warning: anonymous structs are a Microsoft extension
    MOUSEHOOKSTRUCT;
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:6377:5: warning: enumerator value is not representable in the underlying type 'int'
    FEEDBACK_MAX                        = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:12936:5: warning: anonymous structs are a Microsoft extension
    MONITORINFO;
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:12941:5: warning: anonymous structs are a Microsoft extension
    MONITORINFO;
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:14546:5: warning: enumerator value is not representable in the underlying type 'int'
    POINTER_DEVICE_TYPE_MAX            = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\windows.h:167:
#include <winuser.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\winuser.h:14574:5: warning: enumerator value is not representable in the underlying type 'int'
    POINTER_DEVICE_CURSOR_TYPE_MAX       = 0xFFFFFFFF
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:
#include <ole2.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:
#include <objbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:27:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:27:
#include <combaseapi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\combaseapi.h:376:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\combaseapi.h:376:
#include <objidlbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objidlbase.h:7470:9: warning: enumerator value is not representable in the underlying type 'int'
        CO_MARSHALING_CONTEXT_ATTRIBUTE_RESERVED_1      = 0x80000000,
        ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:
#include <ole2.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:
#include <objbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:27:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:27:
#include <combaseapi.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\combaseapi.h:376:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\combaseapi.h:376:
#include <objidlbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objidlbase.h:7471:9: warning: enumerator value is not representable in the underlying type 'int'
        CO_MARSHALING_CONTEXT_ATTRIBUTE_RESERVED_2      = 0x80000001
        ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:
#include <ole2.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:
#include <objbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:107:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:107:
#include <objidl.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objidl.h:11269:5: warning: anonymous structs are a Microsoft extension
    struct _STGMEDIUM_UNION
    ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:
#include <ole2.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:
#include <objbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:394:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:394:
#include <urlmon.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\urlmon.h:1320:9: warning: enumerator value is not representable in the underlying type 'int'
        BINDF_RESERVED_2        = 0x80000000,
        ^
<module-includes>:1:10: note: in file included from <module-includes>:1:
#include "CWin32.h"
         ^
C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:10: note: in file included from C:\cygwin64\home\tumasgiu\workspace\W32ExperimentStepOne\CWin32/CWin32.h:2:
#include <windows.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/windows.h:210:
#include <ole2.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um/ole2.h:32:
#include <objbase.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:394:10: note: in file included from C:\Program Files (x86)\Windows Kits\8.1\Include\um\objbase.h:394:
#include <urlmon.h>
         ^
C:\Program Files (x86)\Windows Kits\8.1\Include\um\urlmon.h:1751:9: warning: enumerator value is not representable in the underlying type 'int'
        BINDF2_RESERVED_1       = 0x80000000
        ^
0x00007FF9920F4FF0 (0x0000B211AE6242E4 0x00007FF99305C1B8 0x00000E8C00000000 0x0000000000008002) <unknown module>
0x00007FF992275D60 (0x0000000000000000 0x00007FF99230B1E0 0x0000000000000001 0x00000000000000C0), InflateRect() + 0xC0 bytes(s)
0x00007FF99226F339 (0x0000000000000001 0x00000000000000C0 0x000000CFF354A898 0x00007FF99225DB1E), GetPropW() + 0x2B9 bytes(s)
0x00007FF99226F23E (0x0000480800000050 0x00007FF9930C4C00 0x0000001E00000000 0x00007FF992250000), GetPropW() + 0x1BE bytes(s)
0x00007FF9930C89D4 (0x00007FF99225CEE1 0x000000CF00000000 0x0000000000000000 0x0000000000000000), KiUserCallbackDispatcher() + 0x24 bytes(s)
0x0000000057341F44 (0x000000CF00000000 0x0000000000000000 0x0000000000000000 0x0000000000000000), NtUserCreateWindowEx() + 0x14 bytes(s)
0x00007FF99225CEE1 (0x0000000000000000 0x000000CFF354ACF0 0x000000CFF354AD40 0x00000000000001C2), CreateWindowExW() + 0x9F1 bytes(s)
0x00007FF992269DF9 (0x0000000000000086 0x0000000000000041 0x0000000000000000 0x00007FF9922578AD), SetWindowLongPtrA() + 0x609 bytes(s)
0x00007FF99227E209 (0x0000000000010007 0x000000CFF354AF29 0x0000000000000086 0x000000000000000E), DialogBoxIndirectParamAorW() + 0x199 bytes(s)
0x00007FF9922DAE5B (0x000000CFF354B160 0x00000000000000A2 0x0000000000007F03 0x00000000000000F3), SoftModalMessageBox() + 0x228B bytes(s)
0x00007FF9922D88E8 (0x00007FF95B5DACC8 0x0000000000000000 0x000002340AE12510 0x000002340FB1E000), MessageBoxW() + 0x348 bytes(s)
0x00007FF9922D8565 (0x0000000000000000 0x0000000000004030 0x000000000000000C 0x000002340FB1E000), MessageBoxTimeoutW() + 0xD5 bytes(s)
0x00007FF9922D8442 (0x000002340B53B670 0x000002340FB1E000 0x000000CFF354B360 0x00007FF95B428470), MessageBoxTimeoutA() + 0x102 bytes(s)
0x00007FF9922D806E (0x000002340D450000 0x00007FF6098F0028 0x000002340D450348 0x000002340D450348), MessageBoxA() + 0x4E bytes(s)
0x000002340D4308E3 (0x00007FF6098F0028 0x000002340D450348 0x000002340D450348 0x00007FF609880028) <unknown module>
0x000002340D450000 (0x000002340D450348 0x000002340D450348 0x00007FF609880028 0x00007FF95B623990) <unknown module>
0x00007FF6098F0028 (0x000002340D450348 0x00007FF609880028 0x00007FF95B623990 0x000000CFF354B370) <unknown module>
0x000002340D450348 (0x00007FF609880028 0x00007FF95B623990 0x000000CFF354B370 0x000002340FB1DFF0) <unknown module>
0x000002340D450348 (0x00007FF95B623990 0x000000CFF354B370 0x000002340FB1DFF0 0x000002340B53B670) <unknown module>
0x00007FF609880028 (0x000000CFF354B370 0x000002340FB1DFF0 0x000002340B53B670 0x0000000000000000) <unknown module>
0x00007FF95B623990 (0x000002340FB1DFF0 0x000002340B53B670 0x0000000000000000 0x0000023400004030), _TWPurGSPx_s8_Pointers
0x000000CFF354B370 (0x000002340B53B670 0x0000000000000000 0x0000023400004030 0x000002340D45039F) <unknown module>
0x000002340FB1DFF0 (0x0000000000000000 0x0000023400004030 0x000002340D45039F 0x0000000000000005) <unknown module>
0x000002340B53B670 (0x0000023400004030 0x000002340D45039F 0x0000000000000005 0x0000000000000000) <unknown module>
```