Preparing for Nightmare Raids
===================

There are certain mechanics in the Nightmare raids that require careful attention and that is difficult without the use of additional tools that the game doesn't provide. Outlined below are the settings required to have ACT call out very important events in NYR and Eidolon. In addition, there are some EffectsUI settings that provide vital insights to things happening to your teammates. Finally, there's a link to a mod which complements many of these settings.

----------


Setting up ACT
-------------

Open ACT and click the "Custom Triggers" tab at the top. For each code snippet below, copy the code and then click the "Import XML" button at the top right of the ACT window.


**New York**

These announce which NPC is pod target.

Alex

> &lt;Trigger R="Mouths of Montauk afflicts Alex with Inevitable Doom" SD="Pod Long Range." ST="3" CR="F" C="New York" T="T" TN="PodLongRange" Ta="F" /&gt;


Mei Ling

> &lt;Trigger R="Mouths of Montauk afflicts Mei Ling with Inevitable Doom" SD="Pod Close Range." ST="3" CR="F" C="New York" T="T" TN="PodCloseRange" Ta="F" />


Rose
> &lt;Trigger R="Mouths of Montauk afflicts Rose with Inevitable Doom" SD="Pod Mid Range." ST="3" CR="F" C="New York" T="T" TN="PodMidRange" Ta="F" />


Zuberi
> &lt;Trigger R="Mouths of Montauk afflicts Zuberi with Inevitable Doom" SD="Pod Zuberi" ST="3" CR="F" C="New York" T="T" TN="PodZuberi" Ta="F" />


----------


**Eidolon**

These announce which Ire buff you received.

Shades
> &lt;Trigger R="Echo of the Outer Dark afflicts you with Shade's Ire" SD="Shades Here" ST="3" CR="F" C="Eidolon" T="T" TN="ShadesIre" Ta="F" />


Deep Ones
> &lt;Trigger R="Frenzied Deep One afflicts you with Deep One's Ire" SD="Deep Ones Here" ST="3" CR="F" C="Eidolon" T="T" TN="DeepOnesIre" Ta="F" />


Drauglings
> &lt;Trigger R="Parasitic Draugling afflicts you with Draugling's Ire" SD="Drawglings Here" ST="3" CR="F" C="Eidolon" T="T" TN="DrauglingsIre" Ta="F" />


----------


**Trigger Timers**

These will announce ahead of time when the next set of adds will appear. Depending on group DPS it's likely you will receive a "<Add Type> Soon" alert when not in Blue Phase, just ignore it.

Add the next set of code snippets in the same way as above, however, note that to check they were added correctly you will need to open your "Spell Timers (Options)" window. This is done by clicking the "Show Timers" button at the top right of the ACT window. A blank window titled "Spell Timers" will appear. Right click inside that window to reveal the "Spell Timers (Options)" window.

Deep Ones
> &lt;Spell N="DeepOnesIre" T="55" OM="F" R="F" A="F" WV="9" RD="T" M="T" Tt="" FC="-16776961" RV="0" C="Eidolon" RC="F" SS="" WS="tts Deep Ones Soon" />


Drauglings
> &lt;Spell N="DrauglingsIre" T="55" OM="F" R="F" A="F" WV="9" RD="T" M="T" Tt="" FC="-16776961" RV="0" C="Eidolon" RC="F" SS="" WS="tts Drawglings soon" />


Shades
> &lt;Spell N="ShadesIre" T="55" OM="F" R="F" A="F" WV="9" RD="T" M="T" Tt="" FC="-16776961" RV="0" C="Eidolon" RC="F" SS="" WS="tts Shades Soon" />


----------


With that all done your ACT should look a little like the following.
![Custom Triggers in ACT](http://i.imgur.com/BKUMwUj.png)

![Spell Timers in ACT](http://i.imgur.com/h6MEp9T.png)


----------


Setting up EffectsUI
-------

For the lazy setup grab a copy of Alice Orwell's EffectsUI settings. However, if you'd rather only add the stuff of interest, here are some of the basic strings you may need.

**New York**

> **String**: Inevitable Doom | show: Pod Target - @owner 
> **Type**: Buff 
> **Monitor recommendations**: Yourself, Raid Group, Defensive Target 
> **Purpose**: Show's who in the raid is the pod target. Useful to set as both a raid
> wide visualiser so you can call it out and a personal warning
> visualiser for when you're the target. If you are the support role
> then you may wish to create an addiational visualiser that will allow
> you to see a warning when your defensive target gets the debuff so you
> know if you need to go out.


----------


> **String**: From beneath*|show: Podded - @owner
> **Type**: Buff
> **Monitor recommendations**: Raid Group
> **Purpose**: See who is podded. Set as raid wide. Sadly can't monitor NPCs still podded in the back.


----------


> **String**: Whisper of Darkness*|show: Whisper - @owner
> **Type**: Buff
> **Monitor recommendations**: Raid Group
> **Purpose**: Monitor stacks on the tanks. If you already monitor stacks in Elite raid then you may want to update your existing string.


----------


> **String**: Gaia Incarnate - Mei Ling | show: @owner
> **String**: Gaia Incarnate - Rose | show: @owner
> **String**: Gaia Incarnate - Alex | show: @owner
> **Type**: Buff
> **Monitor recommendations**: Yourself, Raid Group
> **Purpose**: Not particularly needed but this can used to monitor if you have the circle buff. Good for monitoring just yourself or the
> whole raid incase someone is out of position or bugged.


----------


**Eidolon**

> **String**: Draugling's Ire
> **String**: Deep One's Ire
> **String**: Shade's Ire
> **Type**: Buff
> **Monitor recommendations**: Yourself
> **Purpose**: Shows that you have an add spawned on you. Have the timer show so you can easily see when shades will no longer attack and thus safe for your to resume DPS.


----------


> **String**: Insanity | >5s vanish
> **Type**: Buff
> **Monitor recommendations**: Yourself
> **Purpose**: Shows when you will Insanity dodge. Have the timer show so you can easily see if you will auto-dodge when shades are present
> and thus be ready to attempt an escape.


----------


> **String**: Seeping Terror|show: Terror - @owner
> **Type**: Buff
> **Monitor recommendations**: Raid Group
> **Purpose**: Monitor stacks on the tanks. Same as Elite Eidolon.


----------


> **String**: Call to the Depths
> **Type**: Cast
> **Monitor recommendations**: Offensive Target
> **Purpose**: Not particularly needed but it can be nice to have a jumbo castbar to more easily know when to expect the Ires buff as they
> are applied at the end of the cast.


----------


> **String**: Call of the Abyss
> **Type**: Cast
> **Monitor recommendations**: Offensive Target
> **Purpose**: A couple seconds into this cast you'll receive a random Ire buff so use this to warn yourself to stop everything.


----------


EffectsUI Examples
------------------

If you're a little uncertain how to use the strings above here's a few examples on how to set things up.

 - Monitoring casts by your offensive target - Useful for dangerous casts  https://i.imgur.com/eyK38ib.png - 
 - Monitoring buffs on yourself - Useful for NYR buff circle  https://i.imgur.com/IT1hHrB.png
 - Monitoring debuffs on yourself - Useful for NYR pod target  https://i.imgur.com/Oya0pI8.png
 - Monitoring debuffs on yourself - Useful for Eidolon debuffs  https://i.imgur.com/8XRVMd6.png
 - Monitoring buffs on your raid group - Useful for seeing who has NYR buff circle  https://i.imgur.com/f8DMlfp.png
 - Monitoring debuffs on your raid group - Useful for tank stacks and pod target  https://i.imgur.com/PcWGCVv.png
 - Monitoring debuffs on your defensive target - Useful for support role knowing the filther is pod target  https://i.imgur.com/kHjvyVI.png


----------


Eidolon Helper
--------------

 https://mods.curse.com/tsw-mods/tsw/eidelon_helper

Eidolon Helper is a mod that will help warn you when the 2nd set of adds will appear during Blue Phase, similar to the way the ACT settings above do. As well as doing that, in Flappy NM, this mod will alert you when there is an AEGIS Eruption that matches your shield type, reminding you that you need to go stand in the circle.
