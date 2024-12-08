# PowerShell-Cheat-Sheet

This is the PowerShell cheat sheet with PowerShell commands based on what I learned during the course.

This PowerShell cheat sheet includes the command name, description, syntax, and example for each command.

1. Get-Process

Description: retrieves the local computer's ongoing processes.

Syntax: Get-Process [-Name] <String[]> [-ComputerName] <String[]>  

Example: Get-Process -ComputerName "Server01"

![image](https://github.com/user-attachments/assets/141f5d70-bb82-4a2e-b92c-883e9fb3f21f)

2. Set-ExecutionPolicy

Description: controls how PowerShell is executed on Windows systems.

Syntax: Set-ExecutionPolicy [-ExecutionPolicy] <ExecutionPolicy> [-Scope] <String>

Example: Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser

![image](https://github.com/user-attachments/assets/8f51f1d8-4e9a-454d-959d-f65d2d3770be)

3. Get-Service

Description: provides a list of the mechanism's services' current state.

Syntax: Get-Service [-Name] <String[]>  

Example: Get-Service | Where-Object {$_.Status -eq "Running"}

![image](https://github.com/user-attachments/assets/ee0acb28-a0cd-4cd5-8363-7fcf71858846)

4. New-Item

Description: produces a new object.

Syntax: New-Item [-Path] <String> [-ItemType] <String>  

Example: New-Item -Path "C:\TestFolder" -ItemType Directory 

![image](https://github.com/user-attachments/assets/67793eb1-ec14-4815-9034-dc5912a055d8)

5. Get-EventLog
Description: retrieves information from a local or distant computer's event log.

Syntax: Get-EventLog [-LogName] <String> [-Newest] <Int32>  

Example: Get-EventLog -LogName System -Newest 10

![image](https://github.com/user-attachments/assets/d3397232-8f2c-4757-b867-2bccb591848e)

6. Get-Help

Description: helps with PowerShell operations, processes, and cmdlets.

Syntax: Get-Help [-Name] <String>  

Example: Get-Help Get-Service

![image](https://github.com/user-attachments/assets/fc7c4f73-0dd5-4b9c-b7dc-d324dee7b596)

7. Start-Service

Description: riggers a stopped service.

Syntax: Start-Service [-Name] <String[]>  

Example: Start-Service -Name wuauserv

![image](https://github.com/user-attachments/assets/35dac60d-357c-4811-b4bc-27b7917a4e2f)

8. Stop-Service

Description: Stops a running service

Syntax: Stop-Service [-Name] <String[]>  

Example: Stop-Service -Name wuauserv

![image](https://github.com/user-attachments/assets/46778b17-856c-4cd2-91ce-f6c815f21035)

9. Restart-Computer

Description: restarts the machine, either locally or remotely.

Syntax: Restart-Computer [-ComputerName] <String[]>  

Example: Restart-Computer -ComputerName Server01

![image](https://github.com/user-attachments/assets/171e719c-c3a3-4ea4-a9d4-55e602909566)

10. Test-Connection

Description: transmits pings, or ICMP echo queries, to check for internet access.

Syntax: Test-Connection [-ComputerName] <String[]>  

Example: Test-Connection -ComputerName google.com

![image](https://github.com/user-attachments/assets/a0913129-6983-4cbb-8171-95aac7973d57)

11. Get-Content

Description: retrieves a file's contents.

Syntax: Get-Content [-Path] <String>  

Example: Get-Content -Path "C:\example.txt"

![image](https://github.com/user-attachments/assets/d3c360d6-0159-4356-bc84-a2d99ca93d9f)

12. Export-Csv

Description: saves items to a file after converting them to the CSV format.

Syntax: Export-Csv [-Path] <String> [-NoTypeInformation]  

Example: Get-Process | Export-Csv -Path "C:\processes.csv" -NoTypeInformation

![image](https://github.com/user-attachments/assets/8219d03b-ba4b-47fa-943c-1650472b3919)

13.  Import-Csv

Description: transforms a CSV file into PowerShell objects after reading it.

Syntax: Import-Csv [-Path] <String>  

Example: Import-Csv -Path "C:\data.csv"

![image](https://github.com/user-attachments/assets/7d48d7ff-133c-4b2c-9f6c-8bf67e9f3dde)

14. Remove-Item

Description: deletes registry keys, files.

Syntax: Remove-Item [-Path] <String>  

Example: Remove-Item -Path "C:\OldFiles" -Recurse

![image](https://github.com/user-attachments/assets/a704485c-1336-4179-ab8c-e8021dc0f371)

15. Get-ChildItem

Description: lists each file and folder in a given location.

Syntax: Get-ChildItem [-Path] <String>  

Example: Get-ChildItem -Path "C:\Scripts"

![image](https://github.com/user-attachments/assets/4c7a66d0-4c36-4cb3-87ef-5c61101043d4)

16. Copy-Item

Description: copies folders or files to a different place.

Syntax: Copy-Item [-Path] <String> [-Destination] <String>  

Example: Copy-Item -Path "C:\example.txt" -Destination "C:\Backup"

![image](https://github.com/user-attachments/assets/70499e28-121c-4804-8c2a-153946c2428b)

17. Move-Item

Description: Transfers folders or files to a new location

Syntax: Move-Item [-Path] <String> [-Destination] <String>  

Example: Move-Item -Path "C:\example.txt" -Destination "C:\Archive"

![image](https://github.com/user-attachments/assets/8eb4d2e1-8d1d-4cc1-a9a7-8f55fdace5b1)

18.  Clear-Host

Description: Clears the PowerShell console screen.

Syntax: Clear-Host  

![image](https://github.com/user-attachments/assets/0f1ae954-305a-41fd-8810-25947a1684ae)

19. Measure-Object

Description: determines an object's count, total, and average, among other 
aspects.

Syntax: Measure-Object [-Property] <String> [-Average] [-Sum] [-Maximum] [-Minimum]  

Example: Get-ChildItem "C:\Scripts" | Measure-Object

![image](https://github.com/user-attachments/assets/28c5b35d-4267-4c05-85f5-602776859a2a)

20. Write-Output

Description: transmits output to a pipeline or terminal.

Syntax: Write-Output [-InputObject] <Object>  

Example: Write-Output "Hello, PowerShell!"

![image](https://github.com/user-attachments/assets/1a0e4de6-01e5-427f-92e2-5a9830c71a1e)

21.  Select-Object

Description: chooses particular attributes of unique items or objects.

Syntax: Select-Object [-Property] <String[]>  

Example: Get-Process | Select-Object -Property Name

![image](https://github.com/user-attachments/assets/a2d879a9-3aab-4aa3-b1da-d5c45d77f67b)

22. Sort-Object

Description: sorts objects by property values.

Syntax: Sort-Object [-Property] <String[]> [-Descending]  

Example: Get-Process | Sort-Object -Property WorkingSet -Descending

![image](https://github.com/user-attachments/assets/801fdb68-4781-424a-9e3d-1a06e4872bdd)

23. Read-Host

Description: requests input from the user.

Syntax: Read-Host [-Prompt] <String>  

Example: $Name = Read-Host -Prompt "Enter your name"

![image](https://github.com/user-attachments/assets/0ab57d50-af79-489a-ac07-f719269d7fb7)

24.  Where-Object

Description: filters items according to predetermined criteria.

Syntax: Where-Object [-FilterScript] <ScriptBlock>  

Example: Get-Process | Where-Object {$_.CPU -gt 100}

![image](https://github.com/user-attachments/assets/2f0127dd-0b2a-4496-9605-680864e95cfd)

25. New-Alias

Description: creates a new cmdlet or command alias.

Syntax: New-Alias [-Name] <String> [-Value] <String>  

Example: New-Alias -Name ls -Value Get-ChildItem

![image](https://github.com/user-attachments/assets/b2e59018-ccf5-4311-9670-2e413b8d60d8)

26. Get-Alias

Description: returns a list of every alias that has been defined.

Syntax: Get-Alias [-Name] <String[]>  

Example: Get-Alias -Name ls

![image](https://github.com/user-attachments/assets/2223c9d4-4d88-4c24-a5e6-a115c9a91982)

27. Invoke-Command

Description: executes commands on another or local computer.

Syntax: Invoke-Command [-ScriptBlock] <ScriptBlock> [-ComputerName] 
<String[]>  

Example: Invoke-Command -ScriptBlock { Get-Service } -ComputerName "Server01"

![image](https://github.com/user-attachments/assets/333013de-2db4-464e-a330-d68bfc8d0b04)

28. Add-Content

Description: Appends content to a file.

Syntax: Add-Content [-Path] <String> [-Value] <String>  

Example: Add-Content -Path "C:\example.txt" -Value "New line of text"

![image](https://github.com/user-attachments/assets/ce82342a-aa84-41ce-bbd5-e93cb2079c8c)

29. Remove-Item

Description: Deletes the contents

Syntax: Remove-Item [-Path] <String>  

Example: Remove-Item -Path "C:\example.txt"

![image](https://github.com/user-attachments/assets/94758b6b-559f-431a-b99a-20f7a2a6e8fa)

30. Set-Location

Description: modifies the working directory in use.

Syntax: Set-Location [-Path] <String>  

Example: Set-Location -Path "C:\Scripts"

![image](https://github.com/user-attachments/assets/077e0999-96f4-4f5d-96f3-a4c5d074730b)

31. Get-Location

Description: shows the working directory that is currently in use.

Syntax: Get-Location

![image](https://github.com/user-attachments/assets/972431f0-3e02-460e-9967-1c2222e0bde8)

33.  Compare-Object

Description: shows the differences between two collections of things after comparing them.

Syntax: Compare-Object [-ReferenceObject] <Object> [-DifferenceObject] <Object>  

Example: Compare-Object -ReferenceObject (1, 2, 3) -DifferenceObject (2, 3, 4)

![image](https://github.com/user-attachments/assets/8bc79d74-becc-4e0c-a417-cc34bf5aebd0)






Assignments-

Assignment 1 Cmdlets: 

-$PSVersionTable 

-Write-Host "Hello World!" 

-Get-Service | Where-Object {$_.status –eq "stopped"} 

-$host.version 

-Get-History

-Write-Output 

learned how to use PowerShell commands to monitor command historical events, filter stopped services, verify host version, investigate PowerShell version information, and the results of commands.

Assignment 2 Cmdlets:

-Get help Set-ExecutionPolicy

-Get help Export-Csvsele

-Get help Select-Object

-Get help Get-Process

-Get help Get-EventLog

-Get help Get-Content

Acquired the syntax, application, and specifics of a variety of PowerShell instructions for execution policies, data exporting, object selection, process management, event logging, and content retrieval by using the `Get-Help` cmdlet.

Assignment 3 Cmdlets : 

Get-Process | Export-CSV processes.csv

Get-Process | Export-CSV processes.csv | Out-File Output.txt

Get-Service | Export-CSV serv.csv PS C:\> Get-Service | ConvertTo-CSV

Get-Service | ConvertTo-CSV | Out-File serv.csv

gained the ability to export and transform PowerShell command output, including processes and services, into text and CSV files for distributing and conserving data.

Assignment 4 Cmdlets:

Get-ADComputer   –Filter   *   |   Get-Service   –Name   *

Get-ADComputer   –Filter   *   |   Select-Object   –Property   @{n='ComputerName';e={$_.Name}}   | Get-Service   –Name   *

Get-ADComputer   –Filter   *   |   Select-Object   –Property   @{n='ComputerName';e={$_.Name}}   | Get-WmiObject   –Class   Win32_BIOS   

Get-WmiObject   –Class   Win32_BIOS   –ComputerName   (Get-Content   Computers.txt)   

Get-Process  –Name  *  -ComputerName  (Get-ADComputer  –Filter   *   |                                                                            select-Object   –Expand   Name)   

gained knowledge of how to use PowerShell pipelines and WMI searches to remotely access services, BIOS data, and Active Directory machine properties.

Assignment 5 Cmdlets:

Get-EventLog –LogName Security –Newest 100

$Cred = Get-Credential

Invoke-Command -ComputerName tutu -Credential $cred -ScriptBlockp {Get-EventLog -LogName Security -Newest 100
}

$remote = New-PSSession -ComputerName tutu -Credential $cred

Get-Module -ListAvailable -PSSession $remote

Get-Module

learned how to create PowerShell sessions, get security event logs, handle modules in both local and remote contexts, and utilize credentials to execute commands remotely.

Assignment 6 Cmdlets: 

(Get-CimClass -ClassName Win32_NetworkAdapterConfiguration).CimClassMethods

Get-CimClass -Namespace root/CIMV2 -ClassName *Registration*

Get-CimInstance -ClassName Win32_NetworkAdapterConfiguration | Where-Object {$_.DHCPEnabled -eq $true}

Win32_QuickFixEngineering

discovered how to use PowerShell's CIM cmdlets to acquire systems patch data, filter network adapter settings, and query CIM classes and implementations.

Assignment 7 Cmdlets:

Get-Variable

Remove-Variable -name x

Write-Output $message

learned the procedures for get, remove, and output parameters in order to handle PowerShell variables.

Assignment 8 Cmdlets:

Commands:

1.	for - Iterates over a specified range.

2.	while - Executes a block of code while a condition is true.

3.	Write-Host - Outputs text to the console.

4.	Read-Host - Reads user input.

5.	-match - Compares a string against a regex pattern.

6.	-and - Logical AND operator for conditional checks.

7.	Out-File - Outputs data to a file.

gained knowledge of PowerShell programming, including how to utilize arrays, loops, conditional operators, text matching, user input, and file output.

Assignment 9 Cmdlets:

Get-Service

where-object

$Action = New-ScheduledTaskAction -Execute "powershell.exe" -Argument "-File C:\FILENAME"

$Trigger = New-ScheduledTaskTrigger -AtLogon

Register-ScheduledTask -Action $Action -Trigger $Trigger -TaskName "Show Running Services on Login" -Description "Displays all running services at login"

gained knowledge how to construct scheduled task actions and triggers, filter objects, list services, and register tasks in order to automate the execution of PowerShell scripts upon user login.

Assignment 10 Cmdlets:

New-SmbShare -Name "MESSI" -Path "C:\MESSI" -FullAccess "Everyone"

New-Item -Path "c:\MESSI" -ItemType Directory

Get-SmbShare | Where-Object Name -eq "MESSI"

New-PSDrive -Name "S" -PSProvider FileSystem -Root \\192.168.176.128\\MESSI

learned how to use PowerShell to map networks drives, filter shared data, establish and manage SMB file shares, and then set up folders.
