# Manage Scheduled Tasks in Windows using Powershell

## Create

```powershell
$action = New-ScheduledTaskAction -Execute "notepad" -Argument "file.txt"
$trigger = New-ScheduledTaskTrigger -Daily -At 1pm
Register-ScheduledTask -Action $action -Trigger $trigger -TaskName "Tom - My Task" -Description "Tom's Task"
```

Can't use `:` in the task name!

## List

```powershell
Get-ScheduledTask
schtasks /query
Get-ScheduledTask -TaskName "Tom - *"
```

## Sources

- https://support.microsoft.com/en-us/help/814596/how-to-use-schtasks-exe-to-schedule-tasks-in-windows-server-2003
- https://docs.microsoft.com/en-us/powershell/module/scheduledtasks/set-scheduledtask
- https://docs.microsoft.com/en-us/powershell/module/scheduledtasks
