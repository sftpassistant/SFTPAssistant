# SFTPAssistant
**Secure, automated file transfers for SFTP / cloud workflows**

---

## Overview

**SFTPAssistant** is a Windows desktop utility designed for **automated, unattended file transfer workflows**.  
It is suitable for manual runs, **Task Scheduler**, and **SSIS** scenarios.

SFTPAssistant uses **machine-locked licensing** with secure cryptographic validation.

---

## System Requirements

- Windows 10 / Windows Server 2019 or later  
- .NET Desktop Runtime  
- Internet access (required only for license activation/validation)

---

## Installation

1. Download `SFTPAssistant-Setup.exe`
2. Double-click the installer
3. Complete the installation (installs under `Program Files`)

After installation, SFTPAssistant will be available via:
- Start Menu shortcut
- Installation folder:
  ```
  C:\Program Files\SFTPAssistant
  ```

---

## License Activation (Required)

Before using SFTPAssistant, you must **activate and validate your license**.

### One-time validation step

Open **Command Prompt**, change directory to c:\Program Files\SFTPAssistant and run:

```
SFTPAssistant.exe --validate YOUR-LICENSE-KEY
```

✅ If successful:
- A license file is created under `ProgramData`
- Your license is bound to the current machine
- No further activation is required

### Files created

```
C:\ProgramData\SFTPAssistant\SFTPAssistant\license.json
C:\ProgramData\SFTPAssistant\SFTPAssistant\Logs\SFTPAssistant.Licensing.log
```

---

## Normal Usage

Once licensed, you can run SFTPAssistant normally:
- From Start Menu
- From scheduled tasks
- From automation pipelines

No license dialogs are shown during unattended runs.

---

## Logging

### Licensing logs

```
C:\ProgramData\SFTPAssistant\SFTPAssistant\Logs\SFTPAssistant.Licensing.log
```

Used for:
- License activation diagnostics
- Validation failures
- Recovery guidance

---

## Recovery Scenarios

### Same machine reinstall

Restore the existing `license.json` file to:

```
C:\ProgramData\SFTPAssistant\SFTPAssistant
```

Then re-run `--validate`.

### New machine or machine change

1. Deactivate/reset the license in Lemon Squeezy
2. Re-run:

```
SFTPAssistant.exe --validate YOUR-LICENSE-KEY
```

---

## Where to find your license key

- Purchase confirmation email
- Lemon Squeezy **My Orders** page:
  https://app.lemonsqueezy.com/my-orders

---

## Troubleshooting

If validation fails, check:

```
C:\ProgramData\SFTPAssistant\SFTPAssistant\Logs\SFTPAssistant.Licensing.log
```

---

## Support

Email: **sftpassistant@gmail.com**  
Please include the licensing log when contacting support.

---

## Version

- Current version: **1.0.0**
- Licensing is per-machine

---

## Notes

- Designed for headless execution
- No GUI license prompts
- All licensing actions are logged
