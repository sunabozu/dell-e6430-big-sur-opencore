# Opencore EFI folder for Dell E6430 & macOS Big Sur

Hardware:

- CPU: i5-3320M CPU @ 2.60GHz
- Screen resulution: 1366 × 768
- WiFi: custom DW1510/BCM94322HM8L

What works:

✅ Proper power management, including turboboost (with native SSDTs generated with SSDTtime in Linux)
✅ Sleep, including by closing the lid
✅ HDMI, including sound
✅ Audio with AppleALC
✅ WiFi (`TG80211Family.kext`)
✅ Bluetooth (`BrcmPatchRAM3.kext`, `BrcmFirmwareData.kext`, `BrcmBluetoothInjector.kext`, and `USBInjectAll.kext`)
✅ Backlight with a proper lower level (`SSDT-PNFL` plus `AppleBacklightInjector.kext`)
✅ Trackpad (to enable dragging: `Accessibility` => `Pointer Control` => `Trackpad Options` => `Enable dragging without drag lock`)
✅ 2nd SATA drive in the caddy (via a patch in the `Config.plist`)
✅ Pretty much everything else

Special thanks to [Jake Lo](https://osxlatitude.com/profile/1549-jake-lo/) and [Hervé](https://osxlatitude.com/profile/4953-hervé/).