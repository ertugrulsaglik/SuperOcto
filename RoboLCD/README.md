# Change Log 1.9.0
 - Motor Control redesign
    - Added Motors Off 
    - Added an Extruder Page to control the extruder controls seperately
    - Added ability to heat the extruder from the extruder controls
 - Preheat Wizard
    - Added a feature to add custom Preheat settings
    - Added to the Fine Tune ZOffset Wizard, Change/Load Filament Wizard, Slicer Wizard. You can pick a custom heat for these wizards now
    - Added a Feature to edit/delete any preset
 - Z-Offset Wizard
    - Added in an extra 0.05mm
    - Z-Offset is now measured from the corner
 - Confirmation Screens
    - Added Confirmation screen to Reset EEPROM, Shutdown/Reboot, Reset Connection, and Delete File/Folder
 - Slicer Wizard
    - Added Brim and Raft Support
    - Added Supports from buildplate and everywhere
    - Added the ability to choose the temperature to print with
    - Added Fans on/off functionality
 - Added english.yaml file, which holds all the text for the program
 - Refactored Z-Offset Wizard to use template screens.
    - This change was to fit more language on the screen and auto adjust text as needed.
 - Added a kivy widget that auto adjusts image/text combos
 - Added a workflow to execute a function when backing out of a screen
 - Various text changes
 - Various Icon Changes
 - Bugfix
    - Fixed a bug that caused Anyone with dual extruders on the R2 to crash the screen during the Z-Offset Wizard
    - Fixed bug for disconnecting during an active print, the error message said "printing". It will not populate the correct error


# Change Log 1.8.0
 - Added a Web Cam Toggle Button

# Change Log 1.7.0
 - Print Tuning redesign
    - While printing print tuning will be shown, while not printing only fan controls will be shown
 - New Utilities Functions
    - Motors can be disengaged under Utilities >> Options >> Motors Off
    - You can now reset the connection to the printer at any time through the Utilities >> Option >> Connection tool 
    - Firmware Update has been moved to Options
 - Printer Status Redesign
    - New Non Blocking Error Messages
    - Temperature Controls and Motor Controls have been moved to the printer status screen
    - While Printing the screen will now show elapsed time and estimated time remaining
    - Added a progress bar
 - New Wizard Fine Tune Z Offset
 - New Wizard Bed Level Calibration (R2 Only)
 - fixed up and down buttons to have correctly sized elements
 - various language edits
 - Filament Load/Change will not mess with temperature while printing, it will also set the E-Steps back to where they were
 - Onboard sliced files will now be appended with meta data instead of saved directly with meta data


# Setup
If you want to install this repo:

### if you do not already have RoboLCD on the machine go ahead and clone it
```
git clone https://github.com/Robo3D/RoboLCD.git
```
### if you do have RoboLCD  on the machine pull the updates
```
# Make sure you are in the RoboLCD Folder
cd RoboLCD
git pull
```

### Switch to this branch
```
# Make sure you are in the RoboLCD Folder
cd RoboLCD
git checkout [branch name]
```

### install RoboLCD in develop mode
```
source ~/oprint/bin/activate
# Make sure you are in the RoboLCD Folder
cd ~/RoboLCD
python setup.py develop
```
### restart octoprint and pull up the log 
```
sudo service octoprint restart & tail -f ~/.octoprint/logs/octoprint.log
```



