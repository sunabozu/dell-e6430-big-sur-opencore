# Opencore 0.6.3 EFI folder for Dell E6430 & macOS Big Sur

Hardware:

- CPU: i5-3320M CPU @ 2.60GHz
- Screen resulution: 1366 × 768
- WiFi: custom DW1510/BCM94322HM8L


What works: pretty much everything. Some notes:

| Issue | Description |
| ----- | ----------- |
| SSDT-PM | You **need** to regenerate it for your CPU with ssdtPRGen. See [Opencore guide](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html#sandy-and-ivy-bridge-power-management) |
| Bluetooth | Requires `BrcmPatchRAM3.kext`, `BrcmFirmwareData.kext`, `BrcmBluetoothInjector.kext`, and `USBInjectAll.kext` |
| WiFi | The standard adapter is not supported and was replaced with DW1510. Which is also not supported since Catalina, but we have `TG80211Family.kext` for that |
| Audio | `AppleALC` may cause frezes after waking up, switched to `VoodooHDA` |
| Backlight | The PNLF section **must** be absent in DSDT, and `SSDT-PNFL` should be used with `Whatevergreen` |
| Trackpad | To enable dragging: `Accessibility` => `Pointer Control` => `Trackpad Options` => `Enable dragging without drag lock` |
| 2nd SATA drive in the caddy | Requires a patch in Config.plist |


Special thanks to [Jake Lo](https://osxlatitude.com/profile/1549-jake-lo/) and [Hervé](https://osxlatitude.com/profile/4953-hervé/).
