+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~+
|                  _           _       _                        |
|  _ ____   ____ _| |_ __ ___ (_)_ __ (_)_ __ ___   __ _ _ __   |
| | '__\ \ / / _` | | '_ ` _ \| | '_ \| | '_ ` _ \ / _` | '_ \  |
| | |   \ V / (_| | | | | | | | | | | | | | | | | | (_| | |_) | |
| |_|    \_/ \__, |_|_| |_| |_|_|_| |_|_|_| |_| |_|\__,_| .__/  |
|            |___/                                      |_|     |
|                                                               |
|             github.com/EliederSousa/RVGL-Minimap              |
+~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~+

Configurable ASI mod that adds minimap support to RVGL (Re-Volt) game.  

================================
			TL;DR
================================
Make a copy of you RVGL folder, just to make sure everything will be ok. Download the zip file and extract its contents in your RVGL folder (the same within .exe). That's it.  
PS: The mod disables the multiplayer menu, so you can't play online sessions with it. If you want to get multiplayer menu back, just disable the mod in .ini file or remove the mod from your game folder.

================================
		How to install
================================
Just extract the zip file inside your RVGL folder. Make sure to also extract the folder minimaps, since all images are there. The mod is composed by 3 files (besides the folder and this readme):
  - minimap.asi: The mod itself.
  - version.dll: The ASI loader. This file comes from [Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader), by ThirteenAG.
  - minimap.ini: A configurable file to make the minimap fit your needs. See [Configuration](#Configuration) section.
  
================================
	  Supported versions
================================
I tried to make it work with the latest versions of RVGL. Known versions supported:
23.0602a1
23.1030a1

The game is constantly updated, so don't expect this working in every version forever. I'm focused in Windows x64 system, but Linux and Android support is in the plans... who knows.
  
================================
	A note from the author
================================
This mod disables multiplayer menu, so you can't play online sessions with the minimap enabled. Having a minimap in that context could make some players have a slightly advantage over others, degrading multiplayer experience. I don't want this to happen.

If you want the multiplayer menu back again, you can disable it by editing the .ini file, and changing the option modEnabled to false.


I tried to make a proof of concept to show that a minimap is perfectly possible, even without the right tools. Expect some bugs, lack of transition effects and unfinished things.         

================================
		 Configuration
================================
The .ini file has some options you can change. Let's enumerate some:
  - [default] 
  - modEnabled: You can enable/disable the mod here.
  - consoleDebug: This enables the console output to see some of the player variables while racing. You can use this to get all the necessary info to make more minimaps.
  - sleepTime: Don't mess with this config. It's used to run the mod in the specified frequency, it's not important for you if you doesn't have problems.
 
  - [minimap] 
  - marginLeft, marginTop: In these two configurations, you can put the top/left distance to draw the minimap. Like I said, this mod is not finished, so there are many aspects that I need to improve it. Positioning the image onto the screen is one of them.

  - [nhood1]
  This is example section that configures the minimap for Toys in the hood 1 track. To create your own minimaps, you will need some patience and an image editor. 
  First, create the minimap. I use GIMP to make this, and the **amazing work from Paperman**, without his work I imagine this project didn't even exist. So, you have your minimap, lets configure the ini file:
  
  - minimapMaxSize: Some minimaps are very disproportional (huge width but small height or vice-versa). You can limit the size of image for each track here.  
  - zStartPosInGame: This is the x coordinate of player when race starts. You can take it by enabling debug mode.  
  - xStartPos: Look at your minimap image in some image editor. Can you find the **EXACT** spot where your car starts? So, get the x position of that pixel and put it here.  
  - xOriginPos: Now the most difficult part. You will need to find in your minimap image the pixel that represents the position (0, 0) in the game. **This must be very precisely, or car points will be off image in the minimap.** Enable debug mode, run until you find some place in the map that make X coordinate equals 0, and try to find in the image where is the pixel that represents that position.  
  - yOriginPos: Same as above, but with Z coordinate.

================================
			Backlog
================================
28/11/2023, v0.2.0:
Improvements:
- Support to the latest versions of RGVL (tested in 23.1030a1).
- Now players are coloured circles with black outline to give contrast in some bright tracks.
- Console output changed.

22/11/2023, v0.1.0:
Initial release. 
  
================================
			 Thanks
================================
This project uses images created by Paperman. All credits to him.  
If you are a RVGL dev and want some info about the project, feel free to contact me. See ya.