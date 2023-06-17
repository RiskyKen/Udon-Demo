## **Documentation - Audio Zones**

* * *

==**This documentation is still unfinished!!!**==

* * *

## Installation

==!!! - Import install RiskyKen - Core first - !!!==

Creator Companion Install: Package Install - VRChat Creator Companion

Unity Package Install:Package Install - Unity

* * *

## Prefabs Location
Some parts of the documentation will refer to prefabs that come with Audio Zones. See below for how to find them.

Package install prefabs this will be under: “Assets\RiskyKen\Udon\Utils\Audio Zones\Examples\Prefabs“  
![ab2b35533f99fa923b3b95249f4624de.png](/_resources/ab2b35533f99fa923b3b95249f4624de.png)


Creator Companion install prefabs will be under: “Packages\RiskyKen - Audio Zones\Examples\Prefabs”  


* * *

## Audio Occlusion

Audio occlusion will block the sound of player voices and avatars if they are behind a solid object like a wall.

### Adding Audio Occlusion

Find the `Audio Zones - Manager` prefab then drag it into your scene.

Now right click it and select `Unpack Prefab`.  
![117b4676690e7d1302e249d30ce5c75a.png](/_resources/117b4676690e7d1302e249d30ce5c75a.png)

Lets select the manager and look over some of the options.  

**Update Rate Fast & Slow**  
How long in seconds between player's getting their audio settings updated. Default value `0.00625 = 0.5 / 80` so in a world of 80 players it will take 0.5 seconds for every players audio to get updated. Slow default 0.025 is 2 seconds.

**Target Frame Rate**  
If the frame rate falls below this value the slow update rate will be used otherwise the fast update rate is used.

**Default Audio Channel**  
Default audio channel for players.

**Occlusion Mask**  
What layers Audio Zone will check when determining if a player is behind a wall. *(note adding a lot of layers may hurt performance)*

**Default Audio Settings**  
Audio settings applied to remote players that are **not** occluded.

**Occluded Audio Settings**  
Audio settings applied to remote players that are  occluded.

**Effectors**  
List of audio effectors in the world.  
==Any time an effector *(audio zone or audio pickup)* is added or removed from the world, "Auto Fill Effectors" must be pressed.==  
![6a1faa21c86da410c29d05bf424185e7.png](/_resources/6a1faa21c86da410c29d05bf424185e7.png)

### Custom Audio Settings

Select `Default Audio Settings` under the audio zones manager.  
![346dd857d82182fc1cd53853fb1c1197.png](/_resources/346dd857d82182fc1cd53853fb1c1197.png)

Here we can adjust player voice and avatar audio settings. The settings here are the VRChat defaults. If you ever want to change the audio settings for your world change them here, Audio Zones will override settings from other scripts.  
![cdfd388de8df179314a631d47ef789cb.png](/_resources/cdfd388de8df179314a631d47ef789cb.png)

You can find a detailed discription of each option on the VRChat wiki [player audio page](https://docs.vrchat.com/docs/player-audio) or by reading the tooltips.

Next select `Occluded Audio Settings`.  
![4c9253931592fbfac530ef5db53eb3e5.png](/_resources/4c9253931592fbfac530ef5db53eb3e5.png)  

These are the settings used when a player is behind an audio blocking object like a wall. If you would like the player's voice to still be slightly audible when occluded, increase the voice far and voice gain values by a small amount otherwise leave everything at 0.  
![204c710da52c37733008834eeeff0c6d.png](/_resources/204c710da52c37733008834eeeff0c6d.png)

* * *

## Audio Channels

Audio channels can segregate audio between players without the need for a wall between them. By default all players start in audio channel 0, this can be changed on the audio zone manager if you like.

First drag in the `Audio Zones - Area` prefab into your scene, unpack the prefab then move it to the location you want.  

When selecting the object we can see all the settings for this audio area. Change the audio channel value to a new number like 1. The edit collider button on the box collider can be used to change the size of the zone.
![fa3092c918014dcf791196af8be78677.png](/_resources/fa3092c918014dcf791196af8be78677.png)

Finally select the manager object and press the `Auto Fill Effectors` button.
![1fb0a7ad928963275a67d6258b93265c.png](/_resources/1fb0a7ad928963275a67d6258b93265c.png)
* * *

## Audio Boost

An audio boost or dampen can be applied to zones or pickups, this is ideal or event staff, DJs or a quiet zone.

### Zones
First drag in the 
Temp

### Pickup

Here we will create a pickup that boosts the player’s voice when held.  
Temp

* * *

## Audio Blocking Layer (Advanced)

This section is unfinished.

By default Audio Zones will use objects on the default layer to block audio between players.

Using the default layer is fine for worlds with simple geometry or that will only have a small number of players. However if you are building a world with complex geometry, a large player cap or strict performance requirement, a custom audio blocking layer can be used for better performance and control of Audio Zones.

There are 2 ways a custom audio layer can be setup.

Audio Block Only



Wall Replacement


* * *

## Toggle Audio Zones System

Temp

* * *

## Toggleable Audio Barrier

An audio barrier can be used to toggle audio occlusion in an area. Please read the Audio Blocking Layer section first.
Temp

![9a71be27613b59fbeaf57203aa2bcfd6.png](/_resources/9a71be27613b59fbeaf57203aa2bcfd6.png)

![d5f6a181fe6c23ac49e29cd3db406900.png](/_resources/d5f6a181fe6c23ac49e29cd3db406900.png)

![9471cd6f3c051aadbbcf7cae1bd14cc9.png](/_resources/9471cd6f3c051aadbbcf7cae1bd14cc9.png)

![1c15e53e1bd7bf5ebc6ce65ff9c8deed.png](/_resources/1c15e53e1bd7bf5ebc6ce65ff9c8deed.png)

![161dc130ce8023a39089ced1bcfda984.png](/_resources/161dc130ce8023a39089ced1bcfda984.png)

![c0366228d03f478c17ae70ae3e3aafae.png](/_resources/c0366228d03f478c17ae70ae3e3aafae.png)