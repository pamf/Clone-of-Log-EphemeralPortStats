# Clone-of-Log-EphemeralPortStats

This is just a clone of Log-EphemeralPortStats by Clint Hufman (<https://gallery.technet.microsoft.com/office/Log-EphemeralPortStats-34cc1191>)

```powershell
<#
    .SYNOPSIS
    Runs in an infinite loop getting the TCP ephemeral port and listening port statistics for each local IP address and outputs the data to a text file log.
    .DESCRIPTION
    Runs in an infinite loop getting the TCP ephemeral port and listening port statistics for each local IP address and outputs the data to a text file log. The script writes the ephemeral port stats every 60 seconds by default. To get data from remote computers, this script requires PsExec.exe (SysInternals) to be in the same directory as this script. WARNING: Credentials passed into PSExec are sent over the network in clear text! Prevent this by logging in interactively with a domain account that has administrator rights on the target computers and not specifying credentials to this script. PsExec is a Sysinternals tool owned by Microsoft Corporation. PsExec can be downloaded for free at <http://live.sysinternals.com/psexec.exe>.
    .Parameter CollectionInterval
 This must be an integer in seconds. This is how often you want the script to update the ephemeral port stats and write to the console and to the log. If omitted, 60 seconds is used.
 .Parameter OutputFilePath
 This must be a file path to write to. This will append to an existing text file. If omitted, .\EphemeralPortStats.log is used.
    .EXAMPLE
    .\Log-EphemeralStats.ps1
    This will get TCP ephemeral port and listening port statistics for each local IP address of this computer and outputs the data to a the console and log every 60 seconds by default.
 .EXAMPLE
 .\Log-EphemeralStats.ps1 -CollectionInterval 10
 This will get TCP ephemeral port and listening port statistics for each local IP address of this computer and outputs the data to a the console and log (.\EphemeralPortStats.log is the default) every 10 seconds.
 .EXAMPLE
 .\Log-EphemeralStats.ps1 -CollectionInterval 10 -OutputFilePath '.\output.log'
 This will get TCP ephemeral port and listening port statistics for each local IP address of this computer and outputs the data to a the console and log (in this case .\output.log) every 10 seconds.
    .Notes
    Name: Log-EphemeralStats.ps1
    Author: Clint Huffman (clinth@microsoft.com)
    LastEdit: December 3rd, 2011
 Version: 1.0
    Keywords: PowerShell, TCP, ephemeral, ports, listening
 .Link
 Download PsExec (Sysinternals owned by Microsoft corporation) <http://live.sysinternals.com/psexec.exe>
 #>
```
