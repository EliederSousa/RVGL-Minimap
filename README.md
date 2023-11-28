# RVGL Minimap
Configurable ASI mod that adds minimap support to RVGL (Re-Volt) game.  

<img src="https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/939be166-e096-4141-8c1a-b6020079d85f" align="center" height="250" >
<img src="https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/daa70d57-b042-4292-b63b-a81a90f87ca4" align="center" height="250" >  

## TL;DR
Make a copy of you RVGL folder, just to make sure everything will be ok. Download the zip file from [latest release](https://github.com/EliederSousa/RVGL-Minimap/releases/tag/latest) and extract its contents in your RVGL folder (the same within .exe). That's it.  
PS: The mod disables the multiplayer menu, so you can't play online sessions with it. If you want to get multiplayer menu back, just disable the mod in .ini file or remove the mod from your game folder.

## How to install
First, download the [latest release](https://github.com/EliederSousa/RVGL-Minimap/releases/tag/latest) of zip file. Just extract the zip file inside your RVGL folder. Make sure to also extract the folder minimaps, since all images are there. The mod is composed by 3 files (besides the folder and the readme):
  - minimap.asi: The mod itself.
  - version.dll: The ASI loader. This file comes from [Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader), by ThirteenAG.
  - minimap.ini: A configurable file to make the minimap fit your needs. See [Configuration](#Configuration) section.

## Supported versions
I tried to make it work with the latest versions of RVGL. Known versions supported:  
23.0602a1  
23.1030a1  
The game is constantly updated, so don't expect this working in every version forever. I'm focused in Windows x64 system, but Linux and Android support is in the plans... who knows.  

## A note from the author
This mod disables multiplayer menu, so you can't play online sessions with the minimap enabled. Having a minimap in that context could make some players have a slightly advantage over others, degrading multiplayer experience. I don't want this to happen. 

If you want the multiplayer menu back again, you can disable it by editing the .ini file, and changing this option to false:  
![image](https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/237a6507-c814-45a8-bbd3-e72250c5c369)  

I tried to make a proof of concept to show that a minimap is perfectly possible, even without the right tools. Expect some bugs, lack of transition effects and unfinished things.  

## Configuration
The .ini file has some options you can change. Let's enumerate some:  
  ![image](https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/6b14c4e8-e58a-4d08-a2cc-26a9414e8111)  
  - modEnabled: You can enable/disable the mod here.
  - consoleDebug: This enables the console output to see some of the player variables while racing. You can use this to get all the necessary info to make more minimaps.
  - sleepTime: Don't mess with this config. It's used to run the mod in the specified frequency, it's not important for you if you doesn't have problems.

![image](https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/45d4bc65-01b3-4831-8c90-38b308af6a2d)  
  In those two configurations, you can put the top/left distance to draw the minimap. Like I said, this mod is not finished, so there are many aspects that I need to improve it. Positioning the image onto the screen is one of them.

![image](https://github.com/EliederSousa/RVGL-Minimap/assets/16262291/c29bcf4f-4b8f-4972-ba80-a9c9ca87a6fa)  
  This is example section that configures the minimap for Toys in the hood 1 track. To create your own minimaps, you will need some patience and an image editor. 
  First, create the minimap. I use GIMP to make this, and the **amazing work from Paperman**, without his work I imagine this project didn't even exist. So, you have your minimap, lets configure the ini file:
  
  - minimapMaxSize: Some minimaps are very disproportional (huge width but small height or vice-versa). You can limit the size of image for each track here.  
  - zStartPosInGame: This is the x coordinate of player when race starts. You can take it by enabling debug mode.  
  - xStartPos: Look at your minimap image in some image editor. Can you find the **EXACT** spot where your car starts? So, get the x position of that pixel and put it here.  
  - xOriginPos: Now the most difficult part. You will need to find in your minimap image the pixel that represents the position (0, 0) in the game. **This must be very precisely, or car points will be off image in the minimap.** Enable debug mode, run until you find some place in the map that make X coordinate equals 0, and try to find in the image where is the pixel that represents that position.  
  - yOriginPos: Same as above, but with Z coordinate.

## Roadmap 
  - [x] Displays a minimap (obviously)
  - [x] Let the user put it wherever he wants, with the size he wants
  - [ ] Create minimaps for all original tracks
  - [ ] Create minimaps for most downloaded tracks in [revoltworld.net](https://www.revoltworld.net/)
  - [ ] Minimize bugs
  - [ ] Implement other types of minimaps (make main player be in the center, and move the map and other players)

  If you have any suggestion, minimap request or need help, feel free to contact here.

## Known bugs
  - Minimap doesn't unload properly at end of a race;
  - Minimap is drawn above the pause menu.
  
## Backlog

28/11/2023, v0.2.0:  
Improvements:    
- Support to the latest versions of RGVL (tested in 23.1030a1).
- Now players are coloured circles with black outline to give contrast in some bright tracks.
- Console output changed.

22/11/2023, v0.1.0:  
Initial release.  
  
## Thanks
This project uses images created by Paperman. All credits to him.  
If you are a RVGL dev and want some info about the project, feel free to contact me. See ya.
