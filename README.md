<div align="center">
  <img height="400" src="https://github.com/user-attachments/assets/935ff3cd-dfe1-42f5-875b-8fac5e8da22b">
</div>

> [!WARNING]
> This is just a guide. I don't wrote any of the mods, reshades etc. This is just a set of instructions to help players find a way to play this game. This guide has also some addons for Linux users because there are some extra steps for them to mod the game. Every instructionset with the almighty penguin xD can be safely skipped if you don't use Linux

# General Settings

First of all you should change some settings for both your performance sake and more.

### Upscaling and Frame Generation
- **FRAME GENERATION** : As you should have noticed the game wants you to turn on frame generation real bad when you start it up. This can improve your FPS but **ONLY** when you are already running on stable 60 FPS. So the Frame Generation is really usefull for all of you running a e.g. 1440p or higher monitor
- **AI Upscaling** : Next we have DLSS and FSR. In the game there is no DLSS 4.0 available but you an force it's use thorugh the [Nvidea App](https://www.nvidia.com/en-us/software/nvidia-app/) (resulting in tests by [BenchmarKing](https://www.youtube.com/@benchmarking4386) in higher performance cost). Also if you are using an Nvidea GPU that can run DLSS 4 you might want to install the mod [NVIDIA Streamline update for DLSS 4 FG 310.2.1](https://www.nexusmods.com/monsterhunterwilds/mods/193?tab=description) by [Reiji21](https://next.nexusmods.com/profile/Reiji21). For install check the authors really good instructions.

### Brightness Settings
You should adjust your brightness settings to really improve the games visuals. Although it's not the best option it still works well. Try changing the third brightness to a lower value for best results.

### Other Settings
No other settings will be discussed here because they don't really improve the performance even when lowered. Also dropping a game to the lowest settings to just get it to work should never be an option (although it sadly is in many modern releases).

---

> [!CAUTION]
> This will focus on improving visuals of the game and not improving performance. Only do these steps when you are already running the game with good performance because these changes can have a bit lower performance for more looks

The first step is installing [ReShade](https://reshade.me/) for Monster Hunter Wilds. This will be a variying setup for users so follow your respective guide:

## ReShade Installation <img width="20" height="20" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/windows11/windows11-original.svg"/>
1. Download the installer
2. Install for Monster Hunter Wilds
3. Pick Direct X

## ReShade Installation <img width="20" height="20" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg"/>
1. Download the [reshade-steam-proton](https://github.com/kevinlekiller/reshade-steam-proton) install script by [kevinlekiller](https://github.com/kevinlekiller) with the following command
```console
Hunter@linux:~$ curl -LO https://github.com/kevinlekiller/reshade-steam-proton/raw/main/reshade-linux.sh
```
2. Give the script the right permission by running the following command:
```console
Hunter@linux:~$ chmod u+x reshade-linux.sh
```
3. Run the script and follow though with the installation. Let the script pick the correct things to install to get everything set up right
4. Add this launch option to the game:
```
WINEDLLOVERRIDES="d3dcompiler_47=n; dxgi=n, b" %command%
```

<img height="400" src="https://github.com/user-attachments/assets/8b49ae0b-767a-49b4-8b2c-264980a4fb7c">

## Installing Dependencies
All ReShades need the [REFramework](https://www.nexusmods.com/monsterhunterwilds/mods/93) to work properly so install that. Installation is really easy, just put the `dinput8.dll`in your games directory and you are finished.

## Picking the right ReShade

Next we will need to choose a ReShade. Recommended Reshades are:
- [Wilds Rehydrated - ReShade](https://www.nexusmods.com/monsterhunterwilds/mods/50) made by [ISpectre23](https://next.nexusmods.com/profile/ISpectre23?gameId=6993)
- [Cute preset with ReShade - Tiffany](https://www.nexusmods.com/monsterhunterwilds/mods/52) made by [Kumakichisun](https://next.nexusmods.com/profile/Kumakichisun?gameId=6993)
- ...

Follow your ReShades instructions for installation or just create a folder named something like: `ReShades`, `Shaders` or `ReShade Shaders` in your games directory (You can actually name the folder whatever you want).
Now it's just drag and drop, unzip the files, drag them into the folder you created or into the games directory intself and launch the game. After launch press the `Home` key to open the ReShade menu. Now go up to the top and select the preset you installed.

![grafik](https://github.com/user-attachments/assets/4ea32db0-0e87-4a9f-8413-399eda0ecd52)

---

# Directstorage Upgrade
Capcom somehow screwed up DirectStorage which produces stutters. For a bit more information read the "mods" [description]([DirectStorage](https://www.nexusmods.com/monsterhunterwilds/mods/127))

## Upgrading to Version 1.2.3 <img width="20" height="20" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/windows11/windows11-original.svg"/>
It's pretty straight forward, download the files, then copy them into the games directory. Thats it, this fixes a lot of stutters, nothing that could have been done by CapCom themselves for sure ;)

## Upgrading to Version 1.2.3 <img width="20" height="20" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg"/>
> [!CAUTION]
> Not following these steps when installing on linux can lead to crashes of the entire system, not just the game

1. Download the files
2. Copy your old DirectStorage files: `dstoragecore.dll` and `dstorage.dll` to the following location:
```
/home/<YOUR USERNAME>/.steam/steam/steamapps/compatdata/2246340/pfx/drive_c/windows/system32 
```
3. Replace the old files in the games directory with the new one
4. Add the following launch options to the game
```
WINEDLLOVERRIDES="dstorage,dstoragecore=n,b" %command%
```
<img height="400" src="https://github.com/user-attachments/assets/f42c0063-0f92-45e8-a43c-263229a7a247">


# General Mod Recommendations
These are mods that are here for general performance improvements. Read their mod pages for more information on what they do and how to install them:
- [Wilds OPTIMIZER FPS BOOST LOW CPU CLEANER VISUALS AND BETTER STABILITY](https://www.nexusmods.com/monsterhunterwilds/mods/91)
- [optimization for MonsterHunterWilds GPU AND CPU Performance FPS Optimizer](https://www.nexusmods.com/monsterhunterwilds/mods/88)

_This list is currently not that big because there haven't been that many mods released yet. If you think a mod is missing open an issue._

# Credits
These are all mods used, benchmarkings refered too etc. The creators of all of this content really put in the real work so check them out and give them a like, follow or whatever there is to give xD

### [Digital Foundry](https://www.youtube.com/@DigitalFoundry)
> [Monster Hunter Wilds PC - Profound Perf Problems Must Be Addressed](https://www.youtube.com/watch?v=0yhacyXcizA)
>
> Used their benchmarks and general findings. Great video and definitely worth a watch

### [BenchmarKing](https://www.youtube.com/@benchmarking4386)
> [Monster Hunter Wilds PC | AWFUL PERFORMANCE | Tweaks and Recommendations |](https://www.youtube.com/watch?v=UE35n5tOI1Q&t=328s)
>
> Used the general advise for shading, reshade usage and some of the metrics to get to this standpoint. Also a really nice video with good points and recommendations

### [Reiji21](https://next.nexusmods.com/profile/Reiji21)
> [NVIDIA Streamline update for DLSS 4 FG 310.2.1](https://www.nexusmods.com/monsterhunterwilds/mods/193?tab=description)
> 
> Mod for Nvidea's DLSS 4.0 implementation

### [praydog2](https://next.nexusmods.com/profile/praydog2)
>  [REFramework](https://www.nexusmods.com/monsterhunterwilds/mods/93)
>
> Just an incredible tool for Monster Hunter Wilds modding

### [ReShade](https://reshade.me/)
> A really good tool for modding/improving games

### [kevinlekiller](https://github.com/kevinlekiller)
> [reshade-steam-proton](https://github.com/kevinlekiller/reshade-steam-proton)
>
> Good intallation script to make the reshade installation on linux painfull and easy

### [ISpectre23](https://next.nexusmods.com/profile/ISpectre23)
> [Wilds Rehydrated - ReShade](https://www.nexusmods.com/monsterhunterwilds/mods/50)
>
> Good looking reshade that really improves the game

### [Kumakichisun](https://next.nexusmods.com/profile/Kumakichisun)
> [Cute preset with ReShade - Tiffany](https://www.nexusmods.com/monsterhunterwilds/mods/52)
>
> Good preset that improved the game by a fair amount

### [Darex2094](https://next.nexusmods.com/profile/Darex2094)
> [DirectStorage 1.2.2 Upgrade to 1.2.3 - IO Stutter Fix](https://www.nexusmods.com/monsterhunterwilds/mods/127)
>
> Really cool move to provide the needed files for upgrade

### [VANIILAcoffee](https://next.nexusmods.com/profile/VANIILAcoffee)
> [Wilds OPTIMIZER FPS BOOST LOW CPU CLEANER VISUALS AND BETTER STABILITY](https://www.nexusmods.com/monsterhunterwilds/mods/91)
>
> Nice optimization mod

### [velasquez3589](https://next.nexusmods.com/profile/velasquez3589)
> [optimization for MonsterHunterWilds GPU AND CPU Performance FPS Optimizer](https://www.nexusmods.com/monsterhunterwilds/mods/88)
>
> Good optimization mod
