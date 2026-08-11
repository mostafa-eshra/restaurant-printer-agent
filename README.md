# Innov8 Print Agent Downloads

Official installer and update repository for the Innov8 Print Agent desktop
application.

The application runs in the system tray, connects to an Innov8 POS service, and
delivers receipt jobs to printers on the restaurant's local network. This
repository contains compiled releases only; the source code is maintained in a
private repository.

## Download

Download installers from the [latest release](../../releases/latest).

Choose the correct application variant and operating system:

| Variant | Windows | Linux |
| --- | --- | --- |
| Standalone | `Innov8-Local-Print-Agent-Setup-<version>-x64.exe` | `Innov8-Local-Print-Agent-<version>-x86_64.AppImage` |
| SaaS | `Innov8-SaaS-Local-Print-Agent-Setup-<version>-x64.exe` | `Innov8-SaaS-Local-Print-Agent-<version>-x86_64.AppImage` |

- Use **Standalone** when your configuration requires an API Base URL and API
  key only.
- Use **SaaS** when your configuration also requires a Tenant ID.

Files ending in `.yml` or `.blockmap` are update metadata used by installed
applications. They are not installers.

## Install on Windows

1. Download the appropriate `.exe` installer from the latest release.
2. Run the installer.
3. Complete setup and launch the application.
4. Enter the configuration supplied by your POS administrator, then select
   **Verify and save**.

## Install on Linux

Download the appropriate AppImage, then make it executable and run it:

```bash
chmod +x Innov8-*-x86_64.AppImage
./Innov8-*-x86_64.AppImage
```

The application requires a graphical desktop session with system-tray support.

## Application updates

Installed applications check this repository for newer versions. When an update
is available, the application displays a notification with controls to download
it and restart to install it.

Standalone and SaaS installations use separate update channels, so one variant
will not replace the other.

## Important notes

- Install only the variant assigned by your POS administrator.
- Install one variant per workstation when browser configuration links are used.
  Both variants register the same `innov8posprint` link protocol.
- The workstation must be able to reach both the POS API and its local network
  printer.
- Closing the application window normally keeps the print agent running in the
  system tray. Use the tray menu's **Quit** command to stop it completely.
- Installers are built for 64-bit Windows and 64-bit Linux.

## Support

If configuration verification or printing fails, contact your Innov8 POS
administrator. Do not post API keys, Tenant IDs, configuration links, or other
credentials in public issues.

## License

Copyright © Innov8 Technology. All rights reserved. This software is proprietary
and is distributed only for authorized Innov8 deployments.

