# C++ Reverse Shell dll and exe

This is a simple C++ based reverse shell. You can compile exe or dll.

## Inspired by:
 - https://github.com/dev-frog/C-Reverse-Shell
 - https://github.com/limbenjamin/ReverseShellDll

## Compilation:
exe:
```
i686-w64-mingw32-g++ re.cpp -o re.exe -lws2_32 -lwininet -s -ffunction-sections -fdata-sections -Wno-write-strings -fno-exceptions -fmerge-all-constants -static-libstdc++ -static-libgcc
```

dll:
```
x86_64-w64-mingw32-gcc -shared -o evil.dll dllmain.cpp -lws2_32 -lwininet -s -ffunction-sections -fdata-sections -Wno-write-strings -fno-exceptions -fmerge-all-constants -static-libstdc++ -static-libgcc
```

## How to run dll:
```
rundll32.exe ReverseShellDLL.dll,UniversalSoWhatEverYouTypeHereWillWork
rundll32.exe ReverseShellDLL.dll,CoCreateInstance
regsvr32.exe ReverseShellDLL.dll
msiexec /y "C:\path\to\dll\ReverseShellDLL.dll"
```

