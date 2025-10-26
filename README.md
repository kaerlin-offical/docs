# PowerShell Starter Kit

Use this starter kit to learn how to work with PowerShell, execute commands, write scripts, and customize your environment.

This guide includes examples for:

- Basic PowerShell commands
- Navigation within the file system
- Script creation
- Environment customization
- Use of common cmdlets

---

## Quickstart

### 1. Open PowerShell

Press **Windows + X** → select **Windows PowerShell** or **Terminal (PowerShell)**.\
You can also open PowerShell via the Start menu search by typing:

```
powershell
```

---

### 2. Try basic commands

| Command            | Description                    |
| :----------------- | :----------------------------- |
| `Get-Help`         | Displays help for commands     |
| `Get-Command`      | Lists all available cmdlets    |
| `Get-Service`      | Shows active Windows services  |
| `Get-Process`      | Lists running processes        |
| `Get-Location`     | Displays the current directory |
| `Set-Location C:\` | Changes to another directory   |

Tip: Add the `-Online` parameter to `Get-Help` to open the documentation in your browser.

---

### 3. Create scripts

PowerShell scripts use the `.ps1` file extension.\
Example script:

```
Write-Host "Hello, PowerShell!"
```

Save this as `hello.ps1` and run it with:

```
.\hello.ps1
```

If you receive an error about execution policies, enable script execution with:

```
Set-ExecutionPolicy RemoteSigned
```

Only do this if you understand the security implications.

---

### 4. Install modules

Use the PowerShell Gallery to install modules:

```
Install-Module -Name Az -Scope CurrentUser
```

To update a module:

```
Update-Module -Name Az
```

---

### 5. Test scripts locally

You can test PowerShell scripts directly by navigating to the directory containing your script and running:

```
pwsh .\myScript.ps1
```

Or start an interactive PowerShell session:

```
pwsh
```

---

## Deployment and Automation

If you are using PowerShell scripts in a project or automation pipeline (for example, GitHub Actions or Azure DevOps):

1. Add your script to your repository
2. Commit and push it
3. Reference it in your workflow configuration, for example:

```
- name: Run PowerShell script
  run: pwsh ./scripts/deploy.ps1
```

---

## Troubleshooting

| Issue                   | Solution                                               |
| :---------------------- | :----------------------------------------------------- |
| Script does not run     | Check your execution policy with `Set-ExecutionPolicy` |
| Module not found        | Run `Install-Module <ModuleName>`                      |
| PowerShell not starting | Run as Administrator or check your PATH variables      |

---

## Resources

- Official PowerShell Documentation
- PowerShell Gallery
- [PowerShell GitHub Repository](https://github.com/PowerShell/PowerShell)