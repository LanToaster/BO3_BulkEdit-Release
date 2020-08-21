########################################
################ ReadMe ################
########################################

########################
##### Introduction #####
########################

Welcome and Thanks for your Interest in BulkEdit.
Bo3_BulkEdit is a tool to Modify and convert one or several *.bo3 files and *.schematic files at once according a Ruleset.

The overall Use is fairly Simple, you just drop your Objects and Schematics into the "Source-Objects" Folder, and run Bo3_BulkEdit.exe.
From there BulkEdit will process, according to the Settings, all *.schematic and *.bo3 files in that Folder, and save the Modified Objects to the Results Folder.

Furthermore, if you have the Images, can BulkEdit create simple Preview Pictures of your Objects. .

########################
#### Capabilities ######
########################

A Quick Rundown what Bo3_BulkEdit can do for you:

- Convert *.schematic files to *.bo3 files
- Extract NBT data from Schematics
- Generate Randomised Structures from a set of schematics
- Split single Objects in MultiObject Structures of custom Part Sizes.
- Change/Remove Blocks
- Process PlaceHolder Blocks to:
  Center Objects around a Specific point
  Add BlockChecks
  Add Entities
- Adjust all Settings inside Objects
- Generate a Preview Image of the Object

########################
######## Setup #########
########################

Upon first Start, BulkEdit will create the necessary Folders and Config Files.
Everything Bo3_BulkEdit is supposed to do is Configured in "Bo3_BulkEdit_Settings.ini". - Note: The Indentations/Spaces in front of the Settings are Important.

Schematics and Objects to Process go into the folder: ./Source-Objects/ or ./Source-NBT/
Modified or Extracted Files will be Placed in: ./Result-Objects/ and ./Result-NBT/
 - Note: Different Presets are handled in SubFolders of "/Source-Objects/" and "/Result-Objects/" -

The Various Settings are Explained inside the Config, for more in depth explanation Visit the GitHub page. 

########################
####### Support ########
########################

For Feedback,Support or Questions you can contact me here:
GitHub at: https://github.com/LanToaster/BO3_BulkEdit-Release
Email at: lantoaster@the-sanctuary.info

########################
####### Support ########
########################

Changelog:
21.08.2020 - Initial Release
 - Complete Rewrite of BulkEdit, if you Update from a Previous Version, BulkEdit will upgrade your Configuration.
   Make a Backup to be sure though.