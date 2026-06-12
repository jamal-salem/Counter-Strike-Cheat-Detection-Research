#  01-Binary-Identification

## Example: Calculate SHA256 Hash

PowerShell

```powershell
Get-FileHash .\app.so -Algorithm SHA256
```

Output:

```text
SHA256: 1A2B3C4D...
```

Purpose:
Verify file integrity and identify file versions.

---

#  02-Archive-Inspection

## Example: List Archive Contents

PowerShell

```powershell
7z l ExLoader_Installer.exe
```

Purpose:
Display embedded files without extracting them.

---

#  03-Flutter-Application-Analysis

## Example Flutter Program

```dart
void main() {
  print("Hello Reverse Engineering");
}
```

Build Flow:

```text
Dart
 ↓
Flutter Compiler
 ↓
app.so
```

Purpose:
Understand how Dart becomes native code.

---

#  04-Ghidra-Static-Analysis

## Example C Program

```c
#include <stdio.h>

int add(int a, int b)
{
    return a + b;
}

int main()
{
    printf("%d", add(5,3));
    return 0;
}
```

Expected Ghidra Findings

Functions:

```text
main
add
printf
```

Purpose:
Learn function discovery.

---

#  05-Assembly-Fundamentals

## Example C

```c
int add(int a, int b)
{
    return a + b;
}
```

Possible Assembly

```assembly
push rbp
mov rbp,rsp
mov eax,ecx
add eax,edx
pop rbp
ret
```

Purpose:
Understand compiler output.

---

#  06-Pseudocode-Understanding

## Decompiled Example

Pseudo C:

```c
int FUN_00100000(int a,int b)
{
    return a + b;
}
```

Original Source:

```c
int add(int a,int b)
{
    return a + b;
}
```

Purpose:
Compare original code vs decompiler output.

---

#  07-Anti-Cheat-Detection-Concepts

## Example: Detect Unsigned Processes

PowerShell

```powershell
Get-Process
```

Investigate:

* Unknown executable names
* Unusual memory usage
* Suspicious parent processes

Example Indicators:

```text
unknown.exe
random123.exe
unsignedapp.exe
```

Purpose:
Learn defensive process monitoring.

---

## Example: Active Network Connections

PowerShell

```powershell
netstat -ano
```

Purpose:
Identify unexpected outbound connections.

---

#  08-Learning-Notes

## Example Entry

### Day 1

Tools:

* Detect It Easy
* 7-Zip

Findings:

* PE64
* Visual Studio
* ZIP Overlay

Lessons Learned:

* Not every EXE contains the real application code.
* Installers often contain embedded archives.

---

### Day 2

Tools:

* Ghidra

Findings:

* app.so
* ELF64
* Flutter Runtime

Lessons Learned:

* Decompiled code is not original source code.
* Assembly is closer to machine code than pseudocode.

```
```
