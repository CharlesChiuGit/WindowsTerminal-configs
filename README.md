# WindowsTerminal-configs

### Setup Windows Terminal color schemes

1. Copy & paste the **settings.json** to the Windows Terminal's settings.json

### Apply Oh My Posh

1. Open PowerShell as **Admin**, change PowerShell Excution Policy via:
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```
2. Install Oh My Posh
   ```powershell
   winget install JanDeDobbeleer.OhMyPosh
   ```
3. Edit your PowerShell profile script, you can find its location under the **$PROFILE** variable in your preferred PowerShell version. For example, using notepad:
   ```powershell
   # for powershell
   notepad $PROFILE
   ```
4. Then add the following line.
   ```ps1
   oh-my-posh --init --shell pwsh --config "C:\Users\<username>\AppData\Local\Programs\oh-my-posh\themes\amro.omp.json" | Invoke-Expression
   ```
5. Once added, reload your profile for the changes to take effect.

   ```powershell
   . $PROFILE
   ```
