# Windows 11-Deploading Guide

### Infos:

- Dieser Guide beschreibt nicht, wie man Windows 11 installiert oder neu aufsetzt, sondern nur, wie man nach einer offiziellen Installationsquelle und einem Installationsmedium von Microsoft debloatet.

## Windows Debloat-Script

- Nutzt das [Windows Debloating Script](https://github.com/Raphire/Win11Debloat), um sämtliche Werbung, unnötige Apps und viele weitere Systemanpassungen vorzunehmen.
- Ich empfehle, alles individuell einzustellen und die zu deinstallierenden Apps genau anzusehen, um zu entscheiden, was man behalten möchte.
- Danach läuft Windows mit weniger Ressourcen, belegt weniger Speicher und ist schneller, werbefrei und leichter zu bedienen.

### Falls der Fehler erscheint, dass Winget nicht installiert ist, und ihr es installieren wollt, nutzt diesen Script in einer administrativen PowerShell, um die stabile Version zu installieren:

```powershell
$progressPreference = 'silentlyContinue'
Write-Information "Downloading WinGet and its dependencies..."
Invoke-WebRequest -Uri https://aka.ms/getwinget -OutFile Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
Invoke-WebRequest -Uri https://aka.ms/Microsoft.VCLibs.x64.14.00.Desktop.appx -OutFile Microsoft.VCLibs.x64.14.00.Desktop.appx
Invoke-WebRequest -Uri https://github.com/microsoft/microsoft-ui-xaml/releases/download/v2.8.6/Microsoft.UI.Xaml.2.8.x64.appx -OutFile Microsoft.UI.Xaml.2.8.x64.appx
Add-AppxPackage Microsoft.VCLibs.x64.14.00.Desktop.appx
Add-AppxPackage Microsoft.UI.Xaml.2.8.x64.appx
Add-AppxPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
```

## Ninite

- Nutzt [Ninite](https://ninite.com/), um mehrere verschiedene Apps gleichzeitig zu installieren.
- Es ist empfehlenswert, dies zu tun, bevor man Microsoft Edge deinstalliert (empfohlen, diesen Browser zu entfernen).

## Windows bereinigen

- Öffnet das „Ausführen“-Fenster mit `Windows + R` und gebt „cleanmgr“ ein. Setzt alle Häkchen und führt die Bereinigung durch. Klickt anschließend auf „Systemdateien bereinigen“, um noch mehr Speicherplatz freizugeben.
- Dadurch werden temporäre Dateien gelöscht, und Windows benötigt weniger Speicherplatz.

### Optional: Windows 11 Custom-Theming

- Ihr könnt mein einfaches Paket für individuelles Windows-11-Theming [hier](https://www.mediafire.com/file/7z9fj1xqz3qsugu/SynthWave+84+Theme+Win+11+2+(better).zip/file) herunterladen. Es enthält ein Tutorial (ggf. mit kleinen Fehlern), um sauberes, stilvolles Theming für Windows 11 zu ermöglichen.
