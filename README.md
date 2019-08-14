# XpCounter upgraded from 1.12 to 1.13 by Lavitz
*Version 1.13.2 - Aug 11 2019*

Originally By Thugz [IDF]

XpCounter shows a modified tooltip window for the standard experience bar
containing various experience related information. You can also enable a
dragable frame, that shows those info (or some of them, complete customizable)
on screen.

![](https://cdn-wow.mmoui.com/preview/pvw71495_thumb.jpg)

I will update and clean up this README later. I will also add some features, including labels for the on-screen display and making the on-screen display look much nicer.

If you have any feedback or suggestions, or want to contribute localization or code, please feel free to set up a pull request on GitHub or message me on Discord (Lavitz#1337).

**Links**

- [WillitClassic](https://willitclassic.com/view/IiMqkwBiyonFn9gktunz)
- [WoWInterface](https://www.wowinterface.com/downloads/info25112-XpCounterClassic.html)

FEATURES
--------

- Experience gained in percent
- Experience needed to level up
- Bonus Experience (Rested)
- A reset able Timer that counts XP gained & time played
- EPH - Experience per Hour
- EPM - Experience per Minute
- An estimated value how long it will take you to level up
- Number of Kills and avarage XP per kill
- Number of kills left till level up

Type `/xpcounter` or `/xpc ingame` for more info.

OVERLAY TEXT FORMAT
-------------------

You can set the text displayed in the overlay window with
`/xpc set_overlay_text <text>`. Use the following to insert info:

```
#xp_act#		Actual XP value
#xp_max#		Max XP on this level
#xp_perc#		XP to level up in percent
#xp_left#		XP needed to level up
#xp_rested#		Bonus XP left
#xp#			XP gathered
#time_played#		Time played
#time_left#		Estimated time to level up
#eph#			XP per hour
#epm#			XP per minute
#kills#			Number of mobs killed
#avg_kill_xp#		Average XP rewarded for mob kill
#kills_left#		Estimate number of kills until level up
```

Example:
`/xpc sot #xp_act#/#xp_max# (#xp_perc#% +#xp_rested#) #xp_left# XP left :: #kills# kills (#avg_kill_xp# XP) #kills_left# left :: #XP in #time_played# (#eph# / #epm#) #time_left# left`
`/xpc sot #xp_left# (#avg_kill_xp#) #kills_left# : #time_left#`

TODO
----

* Rewrite the XML for the overlay window
* Add a configuration menu

NOTES
-----

Original author: Thugz [IDF] brutus@ainfos.de

Keeping Data from OLD versions:

To keep your data from pre 0.8 versions just rename `XpBar.lua` to
`XpCounter.lua` in the `SavedVariables` folder of your account. After that,
open the file and replace `XpBar_Config` in the 2nd line with
`XpCounter_Config`.

To migrate your data from post 0.8 versions to versions >= 0.13 just create a
`XpCounter.lua` in the foloowing folder:

`WoWFolder\WTF\AccountName\CharName\SavedVariables\XpCounter.lua`

Copy and paste the lines below and fill in your data for the Char from your old
save file (`WoWFolder\WTF\SavedVariables\XpCounter.lua`).

```
XpCounter_Config =
{
	["played_hours"] = 0,
	["time_update"] = 0,
	["overlay_tooltip_anchor"] = 0,
	["tooltip"] = 0,
	["played_minutes"] = 0,
	["overlay_show"] = 0,
	["overlay_tooltip"] = 0,
	["kills"] = 0,
	["version"] = "13",
	["xp_count"] = 0,
	["avg_kill_xp"] = 0,
	["time"] = 0,
	["overlay_text"] = 0,
	["overlay_locked"] = 0,
	["kills"] = 0
}
```
