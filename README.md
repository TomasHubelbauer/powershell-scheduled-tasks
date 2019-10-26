# Manage Scheduled Tasks in Windows using Powershell

## Create

```powershell
$action = New-ScheduledTaskAction -Execute "notepad" -Argument "file.txt"
$trigger = New-ScheduledTaskTrigger -Daily -At 1pm
Register-ScheduledTask -Action $action -Trigger $trigger -TaskName "Tom: My Task" -Description "Tom's Task"
```
