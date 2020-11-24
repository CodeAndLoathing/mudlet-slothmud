# SlothMap

## Overview 

This is slight repackaging of the **Mudlet SlothMap** package posted by **Bandit/Shatterhand** on the [SlothMud Forum](http://www.slothmud.org/forum//viewtopic.php?f=39&t=4970).

The goal of the repackaging is to make it easier for folks to install by including everything needed to get it running.

## Description 

This package display your current position on the map using MSDP variables to update it "live" as you move about. 

This is a *read-only script* and doesn't include the functions to map new rooms, so you will have to preload it with Bandit/Shatterhand's provided map data from [here](http://www.slothmud.org/forum//viewtopic.php?f=39&t=4970).

I have made the following minor changes:
* Removed unneeded variables accidentally included in the original package. The Mudlet package exporter has (had?) a bug where it includes variables even when not selected.
* Added a line to "register" with Mudlet that a mapper is present, else Mudlet complains.
* Added the OnConnect trigger to enable msdp to report CHARACTER_LOCATION. This may be redunant for some folks but should also be harmless to include it.


## Install Instruction
0) Download the SlothMap.mpackage file and the sloth-map.dat file.
    * [SlothMap.mpackage](https://app.box.com/s/il2lpk701m2u2qwykgox6lxigkr4t4me)
    * [sloth-map.dat](https://app.box.com/s/0mica9lo2dur7pnbvdeydp2zkuc3jew1)

1) Enable MSDP in your profile

   First, load Mudlet with the profile you want to enable this package for.
   The enable MSDP setting is saved by profile.

   Go to Options > Preferences > and make sure that Enable MSDP is checked.
   Note: You have to fully reconnect to Sloth before you will be able to see MSDP variables after enabling them.

2) Uninstall the Generic Mapper

    The Generic Mapper is included by default on all new Mudlet profiles but is not a good option for SlothMud and may interfere with this script. 

    Go to Package Manager > Package Manager
    
    Select generic_mapper, click uninstall.

3) Download & install the SlothMap package

    Go to Package Manager > Package Manager

    Click install, browse to where you downloaded SlothMap.mpackage and install.
    
4) Download & load the SlothMap map data

    Go to settings > Mapper > Press to Choose file and Load

    Browse to where you downloaded sloth-map.dat and load. 

5) Change the end of line delimiter

    Some of the special exits on the map require you to have the end of line delimiter set to ; instead of ;;
    If you want speedwalk to work with these special exits go to Options > Preferences > Input Line
    Change command seperate to just ; instead of ;;

6) Close Mudlet, choose to save your profile

7) Reconnect to Sloth, open the Map with the Map button, and move about.
    If all went well it should pick up your position.

## Uninstall Instructions
If you want to remove the SlothMap.mpackage do so with with the package manager.