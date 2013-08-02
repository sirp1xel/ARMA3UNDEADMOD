ARMA3UNDEADMOD
==============

A configured version of the UNDEAD Mod from ArmA 2 for ArmA 3 Beta (Using All In Arma)

(THIS IS MADE 100% FROM THE USER CHARON, I AM EDITING FILES AND THAT IS ALL TO CONFIGURE FOR ArmA 3!)


   Unsupported Addon
      Use at your own risk
      No responsability for interaction with other addons
      Config , scripts, textures, sounds and music 
      by Charon (charon Productions in the BI forums)
      Adaption,modification or external use is not allowed
      
      VERSION HISTORY :

The Undead V0.84 (31/01/2010):

- Fixed a bug where female civilians would attempt to pick
  up weapons from dead soldiers which resulted in an arma error
  message because female characters can`t use guns

- Static weapons like M2 minitripods on rooftops won`t be
  assigned as target for the zombies anymore

- The antidote injection animation froze the player sometimes
  Now the player is able to move freely after the injection
  animation has been played back

- AI medics will now heal every unit that they normally heal from
  damage ALSO from the infection IF they have the antidote in
  their inventory

- Fixed a bug where some infected towns would not spawn undead on player
  proximity. Now all infected named map locations (Capital/City/villages) 
  spawn undead as intended.

_ Undead won`t chase a helicopter over the whole map. They will "forget"
  about it as a target if it is too far away.
  They will also forget about human characters entering safezones or 
  climbing higher

- Action menu priority for the "inject antidote" has been lowered to be bottom
  of the list, so the player would not inadvertently fire up that action

- Fixed a bug in the control script where a group that has no units added yet
  would not be able to deliver a position for the group leader thus resulting
  in an error message.

- Added a global variable that would if set to true prevent infected
  soldiers that are in the process of becoming undead to use the radio
  CHN_UNDEAD_NOZEDRADIO=true;

- For inexperienced mission makers or to make life easier for the experienced
  a new module has been added. "THE UNDEAD - Spawn Module"
  It automatically spawns undead in regular intervals and thereby creates 
  waves of undead.

- New Global variable CHN_UNDEAD_ZEDLIMIT (100 by default) for the spawn module 

- New undead model for Schnapsdrosel`s excellent BlackOps merc unit (gasmask)
  Install his addon and have the gasmask woodland merc come back as an undead.
  The unit that can be "zombified" is of the type "WDL_Mercenary_Default12"
  Woodland gasmask mercenary
     
  
The Undead V0.83 (27/01/2010):

- Resurrecting undead will now be correctly positioned
  also when they resurrect inside of buildings or bridges

- Custom soldier addons will now be replaced with a generic
  model belonging to the same side as the infected custom soldier

- Zedgroup count works now as intended

- Fixed a syntactical bug in the populate function
  and fixed every zed spawn function so that it would spawn
  zeds also if there is no zed on the map yet (createcenter issue)

- Fixed a significant bug that would cause newly spawned zeds to attack each other
  because they would be declared "human" by another part of the module.
  That also fixes the occasional bad vehicle type :"UNDEAD_UNDEAD_xxxxx" error

- New undead group type with the identifier variable "CHN_UNDEAD_STATICGRP"
  which does not migrate or patrol but does nothing until it spots humans.

- infected soldiers will be audible over radio when they die from the infection.

- New variables : 

CHN_UNDEAD_INITIALIZED : true when the module is initialized

CHN_UNDEAD_ZEDPOPUL1 : true when a town gets populated with undead
by the virtual infection system. Can be set to false again by the mission maker
if he scripts a reaction to the population process.
False at module startup

CHN_UNDEAD_ZEDPOPPOS : contains the position of the populated location

CHN_UNDEAD_ZEDPOPLOCNM : contains the name of the populated location


The Undead V0.82a Mini update (25/01/2010):

Friendly fire handling now works as intended
allowing damage by enemy fire and helicopter crashes
as well as falling damage and being run over by cars


The Undead V0.82 (24/01/2010):

New functions:

[exceptlist] call CHN_UNDEAD_fn_SETMAPINF

[["Chernogorsk"]] call CHN_UNDEAD_fn_SETMAPINF;

Sets all locations on the map to infected status
except the locations in the list (list their name-strings there) 

New feature:

Undead can be completely cured from the infection
with an experimental substance
that can be used in projectiles.

Magazine name: CHN_10Rnd_762_Revert
Ammo name : CHN_762_Revert

- undead won`t seem to be running into the safezone border anymore.
Human targets inside the triggers will be disregarded.

New Global variable:

CHN_UNDEAD_NOMARKS :
if true, then no map infection markers are displayed


The Undead V0.81 (20/01/2010):

Fixed zeds "running in the air" for a too long time in steep terrains

Humans on rooftops or significantly higher altitudes than the zeds won`t be
assigned as their targets anymore

Static weapon crews are now vulnerable to zombie attacks as intended

Friendlyfire works now.
CHN_UNDEAD_FRIENDLYFIR=true in your init.sqf of your mission
enables friendlyfire, but it can`t be turned off at a later point.
But i seriously don`t recommend to allow friendlyfire, you will just got shot 
by your own team members ;)



The Undead V0.8 (13/01/2010):

Cleaned up chats/hints
Fixed slow zed migration bug

The Undead V0.77 (06/01/2010):

Reduced lag of the targetting scripts substantially
Scripts are more efficient now

The Undead V0.75 (12/20/2009):

- Pilots,drivers,crew turn now into zeds inside the vehicles
  with animations and sounds

- New USMC and FR models with textures added

- Headshot option added for corpses

- Resurrection animations added

The Undead V0.75 (12/16/2009):

- Numerous infected sounds added

- Increased attack speed of the infected

- fixed bug that would spawn town guarding zeds upon last zed kill
  when player is in the town

- Global Variables added:

CHN_UNDEAD_NOPILOTKILL
when true: chopper pilots won`t be killed when zeds
huddle around it

CHN_UNDEAD_FRIENDLYFIR
when true: player can be damaged by friendly fire
default is nil, because team mates will oftentimes kill you
when zeds are too close

CHN_UNDEAD_STOP_AL_GORE
when true: no gore and blood effects
default is false

The Undead V0.71 (12/13/2009):

- Location-Logic-based virtual infection management system integrated
  Infected-marked towns will be populated with infected when the player
  gets close to the town

The Undead V0.7 (12/05/2009):

- Envoy system speeds up migration and makes sure that the infection
  does not contain itself when a single human is hidden in a town
  If the envoys or moving whole groups find humans on their way to
  another town, they will now pick up that route again 
  once the humans are killed



The Undead V0.67 (11/29/2009):

- Undead will not intrude into the safezone too much, will return and
  run out of it. That way if the safezone trigger is with a 2-3 m distance
  from the walls, really no undead will be able to enter

- All civilians have an individual texture.


The Undead V0.63 (11/13/2009):

- Major improvement in the collision routines, hardly any undead will 
  pass through walls now. They also collide with each other now !

- Undead will attack humans now when they are en route to other towns

- Civilians now pickup weapons off dead soldiers in their vicinity
  and will engage the undead 

The Undead V0.62 (11/09/2009):

- Safezone script added
- Any medic even ungrouped will heal players if he has the antidote

The Undead V0.61 (11/07/2009):

- Fixed bug that dead undead :D would repeat their dying animation
- Added suitcase "weaponcrate"-object that contains 6 syringes with antidote

The Undead V0.61 (11/06/2009):

- The infected Hound added (Animations,textures,sounds and scripts)
- Civilians try to flee now when attacked


The Undead V0.605 (11/05/2009):

- Widened the completion radius for patrol waypoints,
  so the group is not stuck by inaccessible waypoint locations
- most client-related variables are transmitted now


The Undead V0.6 (11/05 2009):

- Script execution time reduced by a factor of 30
- TCP Animations added
- 

The Undead V0.5 (10/20 2009):

- Undead control scripts written
- Textures made
- Models made

KNOWN ISSUES:


- Blood splatters sometimes mid-air, due to
  faulty Arma2 selection position commands
- Zombies run through walls occasionally.
- Female zombies dont work


DISCLAIMER:

This is NOT an official Addon. Use it at your own risk. We will not be held responsible for any damage these addons might incur.
Nor will we be responsible for any problems you might encounter in installing or using this addon.
