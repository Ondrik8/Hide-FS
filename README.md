# Hide-FS
Inject dll to explorer.exe and hide file from process.

## Requierments:
Microsoft Detours Library - https://github.com/microsoft/Detours

**Compile:**
1. Unzip source code, open command line and enter to source directory
2. SET DETOURS_TARGET_PROCESSOR=X64
3. C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\Build\vcvars64.bat
4. NMAKE

Add detours.lib to Linker additional libraries.

**Hooked Functions:**
- NtQueryDirectoryFile <br>
  Microsoft try to hide it, The address to the function is dynamic, you need to find it yourself.
- RtlUnicodeStringToAnsiString
  
