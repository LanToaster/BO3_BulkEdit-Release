# BO3_BulkEdit

Bo3_BulkEdit is a Tool to Modify/Convert a stack of Bo3 Objects or Schematics for use in TerrainControl or OpenTerrainGenerator

## Bo3_BulkEdit is capable of the Following things:
 - Convert Schematics to Bo3 Objects
 - Extract NBT data from Schematics
 - Generate randomised Structures from a set of schematics
 - Split single large Objects into Structures of custom part sizes
 - Change/Remove Blocks
 - Center objects around Specific Blocks
 - Add BlockChecks
 - Add Entities
 - Change/Set any Setting inside processed or created Bo3 Objects
 - Generate a Preview Image of the Object (Very Slow, but gets the Job done)
 
 
 ## Files and Folders
  - Bo3_BulkEdit will generate all Neccessary Files and Folders (apart from Images for Previews) itself.
  - Bo3_BulkEdit_Settings.ini - Contains all Settings and Instructions for Bo3_BulkEdit.
  - Bo3_BulkEdit_Materials.ini - Contains Conversion Information for Blocks with numeric IDs. This File will be Created from any "level.dat" you place into the Bo3_BulkEdit folder. If you wish to use Modded Blocks it is important to do so. As the Numeric IDs of Modded blocks can and will change.
  - Source-Objects\ - Contains the Source Objects, place files here to Process them. Presets have their own Subfolder
  - Source-NBT\ - Contains the Source Schematics for NBT Extraction. Schematics placed here will only Produce NBT files.
  - Result-Objects\ - Contains the Resulting Objects and Previews. Presets have their own Subfolder
  - Result-NBT\ - Contains Extracted NBT Data. If you Rename them and put them into the Appropriate Subfolder in Result Objects, Blocks with the same NBT data will be Linked to that file.
  - Images\ - Contains the BlockImages used for the Preview of Objects.
 
 # Configuration
 Indentation and Spaces in the Config File are Important for Bo3_BulkEdit, if not used Properly weird stuff might happen.
 
 The Configuration is split up into the overall Settings and Presets. Per default BulkEdit generates only the "DefaultObject" preset.
 Every other Preset will create its own Subfolder in Source-Objects\ and Result-Objects\

## BulkEdit: 
#### DebugMode:
Will Print DebugMessages
#### Logging:
Will Produce a LogFile on Issues/Errors
#### AddNameSpace:
Adds/keeps the "minecraft:" namespace on Vanilla Blocks, when converting a Schematic
#### AddDataValue: 
Will add ":0" as DataValue to Blocks where none is Provided, when converting a Schematic.
#### ShortBlocks:
If true, Lists of Blocks, Branches and similar will use short names. Like: "B()" or "RB()"
## DefaultObject: 
Defaul Preset, Rename this line and Copy all subsequent lines to Create a new Preset.
### Object:
Overall Settings how to handle Objects/Schematics
#### WriteComments:
Determines the Amount of Comments in resulting BO3 files.
#### SplitObjects:
If "true" Splits the Object in Parts
#### SplitSize: 16
The Size of Each individual Part (Centered)
#### StructureMode:
Determines if Schematics in this Preset will be used for Random Structures. For more Information see Further down.
#### Preview: 
If "true" generates a Simple Preview
#### CENTER_Block: 
Object will be Centered around this Block.
#### CENTER_Replacement: 
This Determines the What Happens with the Placeholder for the CenterBlock
#### REMOVE_Blocks: IRON_BLOCK GLASS WOOL:
List of Blocks to be Removed from the Object, this happens before anything else, basically these Blocks will be ignored on Reading the Object. If later Blocks are changed to one of these, they wont be deleted.
#### CHECK_Blocks: EMERALD_BLOCK|Block|Solid 
Generates BlockChecks, Format: PLACEHOLDER|CHECKTYPE|CHECKVALUE the Placeholder Block will be Removed from the Object.
#### BRANCH_Blocks:
Generates Default Branches
#### DefaultBranch: 
The String that gets used as Branch
### NBT:
#### ExtractNBT:
If BulkEdit is supposed to Extract and link NBT data from Schematics.
#### BlackListNBT:
List of Blocks that are Ignored for NBT extraction. Certain Blocks will cause OTG to Crash if you try to use their NBT. 
### Header, Main, SourceBlock, OTG+
All Settings here relate to Settings fround in Bo3 Objects, everything you set here will be applied to the Objects as is. There are no Checks for Valid Settings.
### Blocks:
This is a List of BlockChanges, you can change any BlockString to any other BlockString. Also Block() to RandomBlock()
This is Usefull to attach Specific PreExported NBT data to Blocks, or Change Blocks to RandomBlocks.
Format: - SOURCE BLOCKTYPE -> TARGET BLOCKTYPE | SOURCE BLOCK -> TARGET BLOCK
e.g.
- Block -> RandomBlock | SMOOTH_BRICK:2 -> SMOOTH_BRICK:2,40,SMOOTH_BRICK:1,40,SMOOTH_BRICK,60,COBBLESTONE,50

 # RandomStructures
 ### - Explanation coming Soon(ish) - 
 The System is a Little bit complicated.