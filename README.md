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
4. Launch the tool, enter the url and press enter
