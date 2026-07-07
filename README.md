Useful PowerShell commands for my personal reference. I will keep adding more commands over time.

| Command | What it does |
|---|---|
| Get-Service | Shows all services |
| Get-Service -Name WinRM | Shows the WinRM service |
| Get-Service -ComputerName Client10 | Shows services on Client10 |
| CLS | Clears the screen |
| dir | Shows files and folders in the current directory |
| Enter-PSSession -ComputerName Server1 | Starts a remote PowerShell session with Server1 |
| Get-Process | Shows local running processes |
| Get-Process -ComputerName Client10, Client20, Client30 | Shows processes on multiple remote computers |
| Get-Process \| Out-File C:\myowncomputerprocess.txt | Saves local process list to a text file |
| Get-Process -ComputerName Client10, Client20 \| Out-File C:\processforpouya.txt | Saves process list from Client10 and Client20 to a text file |
| Get-Command | Shows all PowerShell commands |
| Get-Command -Verb Get | Shows commands with the verb Get |
| Get-Command -Verb Remove | Shows commands with the verb Remove |
| Get-Command -Noun Net | Shows commands where the noun is exactly Net |
| Get-Command -Noun Net* | Shows commands where the noun starts with Net |
| Get-Command -Noun *Net | Shows commands where the noun ends with Net |
| Get-Command -Noun *Net* | Shows commands where the noun contains Net |
| Get-Command -Verb Get -Noun Net* | Shows Get commands where the noun starts with Net |
| Get-Help Get-EventLog | Shows help for Get-EventLog |
| Get-EventLog -LogName System -Newest 5 | Shows newest 5 events from System log |
| Get-EventLog -LogName System -Newest 5 \| Format-List \| Out-File C:\pouyabey_log.txt | Saves newest 5 System logs to a text file |
| $ComputerName = "Pouyabey1" | Creates a variable |
| $ComputerName | Shows the variable value |
| Get-EventLog -LogName System -ComputerName $ComputerName -Newest 5 \| Format-List | Uses variable as computer name |
| $num1 = 1 | Creates a number variable |
| $num2 = 2 | Creates a number variable |
| $num1 + $num2 | Adds two variables |
| Get-ExecutionPolicy | Shows current execution policy |
| Set-ExecutionPolicy -ExecutionPolicy Bypass | Sets execution policy to Bypass |
| Set-ExecutionPolicy Bypass | Short version of setting Bypass |
| Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser | Sets RemoteSigned for current user |
