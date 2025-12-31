If you want to help, here is my paypal : [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/sebpoirot)


# QuickHeal Turtle WOW

QuickHeal for Turtle WoW (updated for patch 1.18)

QuickHeal gives healers fast access to all of their direct healing spells for healing party/raid members and themselves. It lets you heal the people who need it, without having to target them manually, or even having to deselect the enemy you're fighting. It gives maximum mana efficiency, and will automatically use a lower rank of healing if the target doesn't need your biggest heal, or if your mana is running low. <Br> 
This also works when not in a party or a raid, and this will save you mana and precious time by automatically selecting the healing spell. <Br> 
There are several different key bindings for constraining the scope of players that will be considered for heals.


## Installation
- Download QuickHeal from this repository into your Interface folder and remove the "-turtle-wow-main" in the folder name

## Usage

**Basic usage**

`/qh help` displays help inside the console<Br>
`/qh cfg` invokes the configuration interface<Br>
To invoke quickheal, make a macro with the `/qh` slash command

**Downrank**

To conserve mana and heal more efficiently you can limit the maximum rank that QuickHeal will use. It is done by moving the slider. on the Downrank Window.<Br>
`/qh dr`: Open the Downrank Window

**High HPS vs Normal HPS**

`/qh toggle`: Toggles between Normal HPS and High HPS. This corresponds to the **Toggle Heathy Threshold 0/100**.  When invoked, it will echo `QuickHeal mode: Normal HPS` and `QuickHeal mode: High HPS` in the console to display its current state.

High HPS is restricted to fast-casting heal spells.
    High healing throughput but low mana efficiency. e.g. Flash Heal

Normal HPS encomapsses ALL healing spells regardless of relative cast time.
    Normal healing throughput with higher mana efficiency.

**Tank list and mt healing**

`/qh tanklist`: Toggles tanklist display.

`+` adds current target into the list.  `C` clears the list.

**Other keybinds for specific healing**

`/qh [mask] [type] [mod]` OR `/quickheal [mask] [type] [mod]`:<Br>

`[mask]`: constrains healing pool to:<Br>
`player`: yourself<Br>
`target`: your target<Br>
`targettarget`: your target's target<Br>
`party`: your party<Br>
`mt`: main tanks (defined in the configuration panel)<Br>
`nonmt`: everyone but the main tanks<Br>
`subgroup`: raid subgroups (defined in the configuration panel)<Br>

`[type]`: constrains healing spell to:<Br>
`heal`: Forces the use of your class' channeled heal spells.<Br>
`hot`: Forces the use of your class' HoT spell over a channeled spell.  Only works for Priests & Druids <Br>
`hs`: Forces the use of Holy Shock for paladins <Br>
`chainheal`: Forces the use of the Chain Heal spell.  Only works for Shamans.<Br>

`[mod]`: optional argument.  Modifies the application of HoTs:<Br>
`max`: force the use of the best HPS Heal or Hot on the next target that is not @100% hp (and that does not currently have a HoT applied if it's a Hot) <Br>
`fh`: firehose mode.  Will apply maximum rank HoT on the next target that does not have a HoT applied.<Br>

`/script QuickHeal(nil,'Spellname')`: this macro is similar to `/qh` but it always try to cast the maximum rank of the specified 'Spellname' on the lowest target. It can be useful for Regrowth if you want to max rank only, or for Swiftmend. <Br>

**QuickHeal Paladin Melee Healing**

The following macros give paladins that choose to heal in melee additional tools to automate Holy Strike and Holy Shock.

`/qh hs`: Holy Shock macro dependant from quickheal rules (general threshold, priority, blacklist...) - Cancels autoattack <Br>

`/run qhHShock(85)`: Other Holy Shock macro independant from quickheal rules (only use MAX rank on the lowest target around) - Number is the min % healing threshold to trigger (DEFAULT is set to 85%) - Doesn't cancel autoattack <Br>

`/run qhHStrike(93,3)`: Specific Holy Strike macro - 1st number is the min %healing threshold to trigger - the 2nd number is the # of targets needed under threshold (DEFAULT set at 93% threshold on 3 targets) <Br>

## ChangeLog:

**Oct 10, 2025**<Br>
- Paladin : replacing /qh hot by /qh hs for paladin only
- Misc : /qh hot doesn't cancel auto attack anymore

**Oct 4, 2025**<Br>
- Paladin : Allowing max rank usage of Holy Shock with "/qh hot max"
- Paladin : Allowing max rank usage of Flash of Light or Holy Light (if active casting buff) with "/qh heal max"

**Sep 21, 2025**<Br>
- Misc : Nampower integration

**Sep 20, 2025**<Br>
- Paladin : Adding melee paladins macros from other fork

**Sep 7, 2025**<Br>
- Paladin : "/qh hot" works again (was always using the damage instead of healing since 1.18 TW patch)
- Misc : Downrank fix for all classes

**Aug 21, 2025**<Br>
- Paladin : Removal of Daybreak which is no longer a heal multiplier in last Turtle Wow patch
- Druid : Talent changes to fit 1.18
- Shaman : Healing way now affects CH/HW and also LHW, after healing power
- Misc : Healcom doesn't autocancel heals anymore (many complains about this mechanic)
- Misc : Bonusscanner no longer necessary (itembonuslib does the job)
- Misc : Mana cost fix on multiple spells

**Jan 31, 2025**<Br>
- Paladin : Integration of Holy Shock logic with the "/qh hot" macro
- Paladin : Holy Shock now use a rank system to limit overheal, updated from 1.17.2 values
- Paladin : Divine Favor is taken in account for holy shock effectiveness
- Paladin : Holy Shock is now usable while moving
- Druid : Improved regrowth is taken in account for Regrowth effectiveness
- Druid : /script QuickHeal(nil,'Swiftmend') now works while moving

**Jan 10, 2025**<Br>
- Shaman : Removal of Purification talent bonus (no longer exist in last Turtle Wow Patch)
- Shaman : Healing Way buff now affects Chain Heal too
- Priest : Holy spells updated for 1.17.2 values
- Priest : Spiritual Healing new value (30% instead of 10%)
- Paladin : Integration of Holy Judgement mechanic to prio HL in that situation
- Paladin : Integration of Daybreak buff detection and multiplier
- Druid : Tree of Life doesn't cancel on quickheal usage anymore
- Druid: Brought back "Cfg->General->Healthy Threshold Slider/RatioHealthy" slider and explanation text; You can now use regrowth even out of combat for Tree of life lovers
- Druid : Brought back low ranks

**Nov 11, 2024**<Br>
- Paladin : Integration of R7 Flash of Light


























