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


## Find version of unity

### Thunderkit
To find the right version Find the Timberborn.exe and look at property's for it.   
there Filevesion is show thats the version of Unity Thunderkit will need.   
at writing its 2022.1.6f1 is know to work

### Mod unity version
this will depend on what version timberAPI uses.  
at writing 2021.3.1f1 is know to work


## Instalation
1. Download [MinimalModSetup](https://github.com/KnatteAnka/MinimalModSetup)  
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
    * this may take some time.
    * it may Crash and need to be closed and opened again and thats normal when changing version or adding alot of new assets.  
    meaning if its stuck importing on one package over 1-2 min then shut it down with taskmanager.
1. Wait for Editor to open
    * if question about Safe mode is shown select  
    if it does press exit safe mode in the top left corner
1. ThunderKit settings window should now show else its found:  
    ![Thunderkit](/assets/images/assetripper/thunderkit.png)  
1. Select thunderkit settings and browse for the timberborn.exe and press import  
![Thunderkit](/assets/images/assetripper/thunderkit_import.png)  
    * this may take some time to import settings
    * it may Crash and need to be closed and opened again and thats normal when changing version or adding alot of new assets.  
    meaning if its stuck importing on one package over 1-2 min then shut it down with taskmanager.
    * When you have the thunderkit window open you can click on Show at startup to have it hidden as default.

## Modding Setup:   
1. close the project and change version to modding version as described above.
1. It will then Open the project, warning may show about version and just click continue
    * it may Crash and need to be closed and opened again and thats normal when changing version or adding alot of new assets.  
    meaning if its stuck importing on one package over 1-2 min then shut it down with taskmanager.
1. Wait for Editor to open
    * if question about Safe mode is shown select  
    if it does press exit safe mode in the top left corner 
1. Try open Assets/Frog statue/FrogStatue.Folktails it should now show settings for the prefab example prefab name.
    * if it does not redo the [Thunderkit](#steps-to-import-game-scripts)
1. up Top you have shortcuts to select mod and action do execute if non is shown:  
"image"
    1. Open Assets/Rebuild and Launch and uncheck and check Quick Access
    1. do the same for any mods manifests
1. you should now be able to select Rebuild and a mod in the list and press Execute to launch the game with that mod.
    * even if it will crash because textures and meshes are missing.       
