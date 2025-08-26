# Git-Powershell-HandyTools
This repository contains commands or files that help you ease your life with daily used commands

| Title              | Description                                                | File Path              |
|--------------------|------------------------------------------------------------|------------------------|
| PowerShell Single Command | Open/Execute a PowerShell script or folder using one command | powershell_profile.ps1 |
| Open apps on boot  | PowerShell script that launches applications                 | open_on_boot.ps1/cmd |

---
## PowerShell Single Command

- Step 1: Open Powershell and type notepad `$PROFILE`.
- Step 2: Add a function like show in powershell_profile.ps1 file in the repository, 
- Step 3: To open a folder use `Set-Location` and to execute a ps1(powershell) script use `&` followed by path.
- Step 4: Save and cloase the file. once done reload profile by using command `. $PROFILE` in powershell.
- Step 5: Now give the function name as command in powershell and boom.

---

## Open apps on boot / Startup Apps Script 

This project provides a simple script to automatically launch your favorite applications (e.g., **Notepad++**, **Visual Studio**, **SSMS**, **Outlook**) every time you boot your Windows machine.

### Features
- Automatically launches multiple apps on startup.
- Works with any executable (just update the paths).
- Simple to install using the Windows **Startup folder**.

### PowerShell Script

```powershell
# List of apps to open at startup

# Notepad++
Start-Process "C:\Program Files\Notepad++\notepad++.exe"

# Visual Studio
Start-Process "C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe"

# SQL Server Management Studio (SSMS)
Start-Process "C:\Program Files (x86)\Microsoft SQL Server Management Studio 19\Common7\IDE\Ssms.exe"

# Outlook
Start-Process "C:\Program Files\Microsoft Office\root\Office16\OUTLOOK.EXE"
```

- Step 1: Save the script above as startup_apps.ps1 in a folder of your choice.
- Step 2: Open the Windows Startup folder by pressing:
- Step 3: Win + R → shell:startup
- Step 4: Create a new shortcut inside the Startup folder with the following target:
- Step 5: powershell.exe -WindowStyle Hidden -ExecutionPolicy Bypass -File "C:\Path\To\startup_apps.ps1"
- Step 6: Restart your PC.
All apps (Notepad++, VS, SSMS, Outlook) should open automatically.

---
