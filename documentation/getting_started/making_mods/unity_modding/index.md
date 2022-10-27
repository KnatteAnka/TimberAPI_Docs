---
title: Unity Modding setup
permalink: /making_mods/unity_modding/
nav_order: 0
layout: page
has_toc: true
parent: Making Mods
---
# Unity Modding setup
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Common Problem:
* Import window:  
    When this window is working it may take some time.  
    It may Crash and need to be force closed and opened again and thats normal when changing version or adding alot of new assets or settings.  
    Meaning if its stuck importing on one package over 1-2 min then shut it down with taskmanager.  
    ![Import Window](/assets/images/Unity_Import.png)  

## Find version of unity

### Thunderkit
To find the right version, find the Timberborn.exe and look at property's for it.   
The Filevesion is shows which version of Unity Thunderkit will need.   
At writing 2022.1.6f1 is known to work

### Mod unity version
This will depend on what version timberAPI uses.  
At writing 2021.3.1f1 is known to work


## Instalation
1. Download Zip [MinimalModSetup](https://github.com/KnatteAnka/MinimalModSetup)  
1. Install [UnityHub](https://unity3d.com/get-unity/download)
1. Open Unityhub/Installs and Click "Install Editor"
1. Select Archive and click download archive and find the versions from above and install those

## Create Project
1. Unpack MinimalModSetup content and rename folder to your liking
1. Open Unityhub/Projects and press Open and select folder from above

## Thunderkit setup:

### Steps to Import game Scripts
1. Change version to use Thunderkit version. (Click on version in column and select the correct one)
1. It will then Open the project, warning may show about version and just click continue

1. Wait for Editor to open
    * If question about Safe mode is shown select.  
    If it does press exit safe mode in the top left corner
1. ThunderKit settings window should now show else its found:  
    ![Thunderkit](/assets/images/assetripper/thunderkit.png)  
    * When you have the thunderkit window open you can click on Show at startup to have it hidden as default.
1. Select thunderkit settings and browse for the timberborn.exe and press import  
![Thunderkit](/assets/images/assetripper/thunderkit_import.png)  
    
    

## Modding Setup:   
1. Close the project and change version to modding version as described above.
1. It will then Open the project, warning may show about version and just click continue
1. Wait for Editor to open, This may take some time
    * If question about Safe mode is shown select.  
    If it does press exit safe mode in the top left corner 
1. Try open Assets/Frog statue/FrogStatue.Folktails it should now show settings for the prefab example prefab name.
    * if it does not redo the [Thunderkit](#steps-to-import-game-scripts)
1. Up Top you have shortcuts to select mod and action do execute if non is shown:  
"image"
    1. Open Assets/Rebuild and Launch and uncheck and check Quick Access
    1. Do the same for any mods manifests
1. You should now be able to select Rebuild and a mod in the list and press Execute to launch the game with that mod.
    * even if it will crash because textures and meshes are missing.       

## Update or add mod to Unity launch
1. Download mod to update or add
1. Open Packages\BepInExPack_Timberborn\BepInExPack_Timberborn\BepInEx\plugins
1. Remove if mod folder if it already exists
1. Copy downloaded mod to the folder
1. next time you Open the project, it will import the mod, This may take some time

## Export/Import package
This can be used to transfer assets from Assetripped game to your mods project
1. Select any amount of assets and right click and select Export package
2. To import it in the next one right click in project view and select Import package/Custom package

## Export/Import FBX files
This is used if you want to export to be able to import in blender or other cad programs.  

### Install Plugin
1. Open Packet manager under Window 
2. Search for FBX and install FBX Exporter
3. Open Project settings under Edit
4. Select FBX Export and change Export Path to your liking
5. And change Export format to Binary

### Export File
1. Open an/the Asset you want to export 
2. Select what you want to export in the hierarchy view
3. Right click an select Export to FBX

### Import File
1. Before you use a new file select the FBX file and Enable read/Write under Model/Meshes
1. Files can then be dragged in to any asset and used


## Good to know stuff
### Components:
1. Box Collider and Capsule Collider are examples of a component type used on _Finished/_Unfinished/Part to specify if building should be selected when clicked on an location.
2. Cluster Element Specification is if building should be connected and share power and what position
3. Look at existing buildings to see what components is needed for some functions
4. Block Object Nav Mesh Settings need to have "Generate Floors on Stackable" enabled to link path to stuff built on top of building

### Modeling:
1. When exporting FBX files it also exports Textures but when importing of any change in example Blender is done it may be need of    replace texture and in blender it is good practice to change name of texture so its easy to find correct textures.    
