# PrusaSlicer 2.6 AnkerMake Community Profiles

[![GitHub release](https://img.shields.io/github/v/release/Ankermgmt/prusaslicer-ankermake-ce-profiles?display_name=tag&sort=semver&style=for-the-badge)](https://github.com/Ankermgmt/prusaslicer-ankermake-ce-profiles/releases/latest)

![image](https://github.com/Ankermgmt/prusaslicer-ankermake-ce-profiles/assets/10281380/77beb5cb-c6cb-4385-a266-0ff0e30ac9c2)

## Overview

This repository holds the latest version and updates to AnkerMake M5 andAnkerMake M5C community profiles for the [initially developed and maintained by @just-trey](https://github.com/just-trey/ankermake-m5-profile). We have decided to continue to support these profiles to allow users an alternative to the official profiles provided by AnkerMake. You can install these profiles alongside the built-in AnkerMake profiles. Why not install both and see which one you prefer?

### "FAST" modes

Please note that the FAST profile included is NOT the max acceleration and speed the printer can perform. Higher speed can be achieved by adjusting the speed and acceleration. We found the setting (thanks @Xelinor) provided to be the best compromise for quality vs. speed.

### A note about z-lift

We have z-lift disabled by default as it impacts print times. If you find your nozzle scraping surfaces, plan on manual filament changes mid-print, or are using ironing, enabling z-lift is highly recommended. We recommend at least a .25 z-lift height.

## Known Issues

- The speed multiplier (ex x1.8) is not correct.
- Changing speeds via the touch screen or app after printing starts is not working

## Note

The configuration authors strongly believe there is no "one size fits all" profile. These profiles provide an excellent base to get started, but we highly encourage users to learn and adjust their slicer settings to suit their use case.

## Installing the profile

You have 3 ways provided to install the profiles:

- [Scripted Install](#scripted-install)
- [Manual Install](#manual-install)
- [Import Profiles](#import-profiles) (only recommended for installing into AnkerMake_alpha slicer and Super Slicer)

For all options, be sure to download [PrusaSlicer-AMCE-Profile.zip](https://github.com/Ankermgmt/prusaslicer-ankermake-ce-profiles/releases/latest/download/PrusaSlicer-AMCE-Profile.zip)

### Scripted Install

We now provide Bash and Powershell scripts to make installing/updating these profiles easier.

Run `./install.sh` or `./install.ps1` to install/update the profiles.

1. Extract the zip files (Our example uses the download directory)
2. Open the terminal/PowerShell window
3. `cd ~/Downloads/PrusaSlicer-AMCE-Profile`
4. On windows, depending on your Execution policy, you may need to change the execution policy to run the powershell script. Use the following to change
   the execution policy for the current terminal session only by opening a powershell prompt in the current directory and then typing `Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process`
5. run `./install.sh` (mac/Linux) or `.\install.ps1` (windows)
6. [Add the printer](#adding-the-printer-only-needed-for-scripted-install-and-manual-install)

### Manual Install

1. Open PrusaSlicer
1. Under the Help Menu, choose "Show Configuration Folder" (keep this folder open for the next several steps).
1. Close out of PrusaSlicer
1. Extract the zip file to a location of your choice and open the folder.
1. Copy the *"vendor"* folder to the Configuration folder you opened in step two.![image](https://user-images.githubusercontent.com/10281380/209450820-d98c5f82-07d5-453b-b5e1-11b294b257ac.png)
6. [Add the printer](#adding-the-printer-only-needed-for-scripted-install-and-manual-install)

### Import Profiles

1. Extract the zip file to a location of your choice and open the folder.
1. Open the AnkerMake Alpha slicer
1. Go to File -> Import -> Import Config Bundle
2. Locate 'AMCE_config_bundle.ini' in the extracted zip location and click open.
3. On the printer setting panel, select 'AnkerMake M5 (0.4 nozzle) @AMCE' or 'AnkerMake M5C (0.4 nozzle) @AMCE', then choose the filament and Print settings you would like to use.

## Adding the printer (only needed for Scripted Install and Manual Install)

1. Open PrusaSlicer and you should now be able to add a new AnkerMake M5 or M5C CE Printer. (printer Settings tab → Printer drop-down → Add/remove printers
1. In the Configuration Wizard, choose Other Vendors:
1. Select the AnkerMake CE Checkbox
1. Select AnkerMake CE FFF under the left menu
1. Ensure the check mark next to the 0.4 mm nozzle is enabled.
1. In the left Navigation, select Filaments and then select all available filaments.  
1. Once you have added any other printers or made changes, click Finish on the Configuration wizard.

## How to print via wifi after slicing

Printing files via wifi is supported but not directly from PrusaSlicer. You may print via wifi using the AnkerMake Slicer.

### Steps

1. Slice and save your gcode to a location of your choice
1. Make sure your AnkerMake M5 printer is on and connected to wifi
1. Open the AnkerMake Slicer
1. Click on the Device tab
1. Click on the My Computer icon and select your sliced file. ![image](https://user-images.githubusercontent.com/10281380/206552887-486043c2-3329-4105-ad99-438bf1f64516.png)
1. Click print underneath the device details. ![image](https://user-images.githubusercontent.com/10281380/206553190-b5b8a1b8-454d-46a1-8b97-368d6a0632d6.png)

## Licences

- Prusa profiles are under-released under the [GNU AFFERO GENERAL PUBLIC LICENSE](LICENSE).

## Changelog

[View Changelog](/changelog.md)
