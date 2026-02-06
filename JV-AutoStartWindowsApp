$TaskName = "JV-StartWindowsApp"

$Action = New-ScheduledTaskAction `
    -Execute "explorer.exe" `
    -Argument "shell:AppsFolder\MicrosoftCorporationII.Windows365_8wekyb3d8bbwe!Windows365"

$Trigger = New-ScheduledTaskTrigger -AtLogOn

$Principal = New-ScheduledTaskPrincipal `
    -GroupId "BUILTIN\Users" `
    -RunLevel Limited

Register-ScheduledTask `
    -TaskName $TaskName `
    -Action $Action `
    -Trigger $Trigger `
    -Principal $Principal `
    -Force
