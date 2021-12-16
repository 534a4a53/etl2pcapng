Start the log collection:
Run the network trace on the VDA via an RDP connection over an elevated CMD prompt.
c:\> netsh trace start capture=yes tracefile=c:\net.etl persistent=yes maxsize=4096

capture =yes (ensures network trace is captured)
persistent  =yes (specifies whether the tracing session continues  across reboots, and is on until netsh trace stop is issued)
tracefile= %LOCALAPPDATA%\Temp\NetTraces\NetTrace.etl (specifies location of the output file, default is present here)
 
  Stop log collection:
Logon to the VDA and stop the network trace
c:\> netsh trace stop
 
Collect the following files:
C:\net.etl -> It is same as a capture file.
C:\net.cab -> Contains TXT files with the report and a report.etl which is same as net.etl
 
c:\net.etl could be viewed in Microsoft Network Monitor 3.4 (https://www.microsoft.com/en-in/download/details.aspx?id=4865) OR  Microsoft Message Analyzer (https://www.microsoft.com/en-in/download/details.aspx?id=44226).

See here for full data: https://support.citrix.com/article/CTX214599