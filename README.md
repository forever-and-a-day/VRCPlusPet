# VRCPlusPet-Free
<!-- general TODO: tweak WhiteSnowflake's instructions to mention mod config in UIX, and update mentioned prefs to not be out-of-date w/in-game ones -->
<!-- Note to self: consider reuploading text bubble image to other hosting provider, discord cdn might not be the best especially since you need it to use said feature -->

As a plus subscriber myself, I don't VRCat is a significant driver of subscriptions. Enjoy!

VRChat Mod that uses [MelonLoader](https://github.com/HerpDerpinstine/MelonLoader). <br>
Hides VRC+ advertising, can replace default pet, his phrases, poke sounds and chat bubble.

<h3>Notice!</h3>
This mod in its current state, breaks emmVRC's Plus check. This is not an intended function. Please be aware that abusing this mod to add emmVRC Favorites is abuse of the emmVRC Network! Doing so will likely result in a ban if (again, likely) emmVRC moves to checking your supporter tag server-side with their own servers. DO NOT add emmVRC Favorites without VRC+. If you get VRC+, you don't even need this mod, just use the original by WhiteSnowflake! This mod is intended only to let free users use/customize the cat, or remove the VRC+ ads if you don't use emmVRC.<br>
<br>
If someone knows how to make this not interfere with emmVRC, *please* submit a pull request! I don't know C#, unfortunately, but will accept commits that clearly aren't malicious or obfuscated! Same goes for maintenance or improvements! <br>
<br> <!-- wtf github why ur markdown so weird? the first and second paragraphs have line breaks already but I need a fucking br tags to everything to get one here??? -->
If your name is Emilia or you otherwise develop for emmVRC, I would *strongly* recommend you preform your VRC+ checks from your own server at game run time using the Player API and the system_supporter tag, then have the local mod pull that information from your server (and reject new favs server-side if the local mod sends them anyway). If this method is truly technically impossible, please let me know on discord (forever-and-a-day#3000) and I'll take this mod down. 


<h3>Main Features:</h3>
 
 * All features can be enabled/disabled;
 * VRC+ advertising hiding (w/o hiding "Early Supporter Badge" and "Supporter Badge");
 * Changing main menu tab buttons to normal size;
 * Custom pet image;
 * Custom pet phrases;
 * Custom pet poke sounds;
 * Custom chat bubble image (text background). <br>

![Natsuki preview](https://i.ibb.co/txdSMpn/2020-12-30-054613.png)

<h3>Requirements:</h3>

 1. [MelonLoader](https://github.com/HerpDerpinstine/MelonLoader/releases) (min. v0.3.0);
 2. [UIExpansionKit](https://github.com/knah/VRCMods/releases/tag/updates-2021-02-02).

<h3>How to install from releases:</h3>

> VRChat game folder: Steam Library -> RMB on VRChat -> Properties -> Local Files -> Browse Local Files.

Just drop "VRCPlusPet-Free.dll" from the releases section of this page to "VRChat/Mods" folder.
 
<h3>How to build and install from source (best practice):</h3>

0. Make sure you have Visual Studio ([2019](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=16#)
 is fine) installed - Other IDEs will likely work, but then you prob know what you're doing
1. Clone this repository or click green Download Code button, then Download ZIP (extract the zip)
2. Open the directory where you cloned/extracted the code
3. Copy all the DLLs from {VRChat-INSTALL-DIR}\MelonLoader\Managed to the "References" Folder
4. (Unknown if necessary, won't break anything) Copy {VRChat-INSTALL-DIR}\MelonLoader\MelonLoader.dll into the "References" Folder <!-- TODO: try to build w/o melonloader.dll and see if broke or nah -->
5. Copy {VRChat-INSTALL-DIR}\Mods\UIExpansionKit.dll into the "References" Folder
6. Open VRCPlusPet.sln in Visual Studio
7. Expand the project in the tree on the right and check for creepy code in the files (references to weird websites, auth tokens, etc) or obfuscation (single character C# filenames, randomized variable names, code that you're pretty sure a human programmer wouldn't understand, etc) 
8. Once you're absolutely sure it's safe, open the "Build" menu at the top and choose "Build *ProjectName*", usually "Build VRCPlusPet" or "Build VRCPlusPet-Free"
9. In a few moments, a folder should appear in the project directory named "Output", and inside that, "VRCPlusPet". Rename VRCPlusPet.dll to something like VRCPlusPet-Free.dll to avoid confusion with the original, if you want, then copy it into {VRChat-INSTALL-DIR}\Mods. 
10. You can now run the game. Enjoy! 
 
<h3>Mod configuration</h3>

All configs is placed in the in the Mod Settings menu that placed in the lower right corner of VRChat's Settings menu. <br>
Game restart needed after changing.

<h3>How to disable/enable VRC+ advertising?</h3>

 1. Enable/Disable "FAKE VRCP" in mod config.

<h3>How to replace Pet image?</h3>

  > Mod currently supports only ".png" image files. <br>
  > Image file name must be "pet.png". <br>

  1. Enable "Replace pet image?" in mod config;
  2. Open VRChat game folder (Steam Library -> RMB on VRChat -> Properties -> Local Files -> Browse Local Files);
  3. Drop image file to "UserData/VRCPlusPet_Config/" folder (make sure that file has name "pet.png").

<h3>How to replace Chat Bubble image?</h3>

  > Mod currently supports only ".png" image files. <br>
  > Image file name must be "bubble.png". <br>
  > Image editing required. <br>
 
  1. Download original image: [Click me >_<](https://cdn.discordapp.com/attachments/548545237123989505/793646716779364362/ChatBubble_IMG_UI.png);
  2. Edit the image as you want;
  3. Enable "Replace bubble image?" in mod config;
  4. Open VRChat game folder (Steam Library -> RMB on VRChat -> Properties -> Local Files -> Browse Local Files);
  5. Drop image file to "UserData/VRCPlusPet_Config/" folder (make sure that file has name "bubble.png").

  > [Green version from the screenshot](https://media.discordapp.net/attachments/674717751662739478/813119607854202880/bubble.png)

<h3>How to replace Pet Phrases?</h3>
  
  1. Enable "Replace pet phrases?" in mod config (for auto-creating files - game restart needed);
  2. Open VRChat game folder (Steam Library -> RMB on VRChat -> Properties -> Local Files -> Browse Local Files);
  3. Change files in "UserData/VRCPlusPet_Config/" folder.

  > "normalPhrases.txt" - Random phrases. <br>
  > "pokePhrases.txt" - Random Phrases when poking.
  
<h3>How to replace Poke Sounds?</h3>

  > Mod currently supports only ".ogg/.wav" sound files. <br>
  > Sound files can have any names. <br>
  
  1. Enable "Replace pet poke sounds?" in mod config (for auto-creating folder - game restart needed);
  2. Open VRChat game folder  (Steam Library -> RMB on VRChat -> Properties -> Local Files -> Browse Local Files);
  3. Drop audio files to "UserData/VRCPlusPet_Config/audio/" folder.
 
<h3>Warning</h3>

  I'm not responsible if you get banned or anything like that! Use this mod at your own risk.
 <!-- maybe add emmvrc disclaimer here too? I think it might be redundant given the mentions earlier -->
<h3>Credits</h3>
 
  1. Original idea - [VRC-Minus](https://github.com/HerpDerpinstine/VRC-Minus) by HerpDerpinstine;
  2. [UIExpansionKit](https://github.com/knah/VRCMods) by knah;
  3. [MelonLoader](https://github.com/HerpDerpinstine/MelonLoader) by HerpDerpinstine.
<!-- add link to original mod or are previous mentions and fork links enough? will think on and prob forget -->
