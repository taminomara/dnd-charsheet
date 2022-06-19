# DnD charsheet

Current release: [v0.1] (see an [example], my lvl5 artificer Nissa). Make a copy and fill in for your character!

*Note: this is an alpha release. I'm fairly new to DnD, so some functionality may be missing.*
*Please [report any bugs and feature requests] to this repo.*

[v0.1]: https://docs.google.com/spreadsheets/d/1CUvzUhWbFLaV_pfz20NMdJCa-dJ7vRbiKOHLn0vZgXY/edit?usp=sharing
[example]: https://docs.google.com/spreadsheets/d/1eInNnRA1s2wx3-wW0L9C2Dzz4jeJA5OS3K8GeLl9hyA/edit?usp=sharing
[report any bugs and feature requests]: https://github.com/taminomara/dnd-charsheet/issues

----

This is a charsheet template made in google sheets, offering you these nice benefits:

- Powerful formulas form the box.
  You don't have to re-calculate everything whenever you level up or take a debuff,
  the sheet will do everything for you.
- Flexibility and versatility.
  This sheed doesn't pretend to be an app, it has no locked ranges or strict rules
  on how to use it. If you find any functionality missing, or doesn't fit your purposes,
  just edit it, or maybe even delete all the formulas and fill the data yourself.
- Good documentation, which includes UI and formulas.

If you like spreadsheets but don't want to waste days creating your own,
this is a good point to start!

----

<img width="1117" alt="image" src="https://user-images.githubusercontent.com/81165235/174246117-2a1cd3d0-c99a-4c77-a5a8-0c1ccc2fb1c4.png">

----

## Documentation

There are three sheets in the document:
*Character* is the actual charsheet,
*Notes* is for any notes and links you may want to save,
*Aux* is for auxiliary things used in formulas.

The charsheet is split into five sections:
character stats, features and notes, spells and actions, weapons, inventory.

Formulas in these sections sometimes use absolute column references,
so you can't move sections horizontally. Formulas never use absolute row references,
so you can move them vertically, rearrange them or copy them.
See chapter on [having multiple characters on one sheet](#having-multiple-characters-on-one-sheet)
for more info.

## Character stats

The section contains basic stats automatically canculated from your class, level and base characteristics.

- **Name, race, alignment, age, appearance, lanuages** are just text cells that you may fill with anything you like.

- **Class** is a dropdown with standard classes. If you're playing a custom class, add it [at the *Aux* sheet](#aux-sheet).

- **Inspiration** is a checkbox for tracking if you have one.

- **HP** shows your HP.
  - **Base** is your maximum HP.
    By default, it is calculated as an average dice roll for your class per level.
    If you want to throw dices instead, scrap the formula and fill the cell with a custom value.
  - **Dmg** is for keeping track of all damages and heals.
    When you take damage, substract HPs from this cell value.
    When you heal, add HPs to this cell value.
    The value in this cell should always stay negative.
  - **Temp** is for keeping track of temporary HPs given to you by spells.
    When you're assigned temp HPs, save them to this cell.
    When you're taking damage, substract HPs from this cell first,
    then substract anything that's left from the *Dmg* cell.
    When you heal, do not restore temporary HPs.
    
- **Speed** shows your speed.
  - **Base** is your base walking speed, you should set it based on your race.
  - **Temp** allows you to temporarily override base value.
  - **Mod** allows you to add a modifier to your base value.
  If you're wearing an armor that you have not enough strength for,
  this is also taken into account when calculating your final speed.
  
- **AC** shows your armor class and contains other armor settings.
  - **Base** is the armor class for the armor you're wearing.
  - **Mod** allows you to add a modifier to your armor's base class.
  - **Dex <** limits your desterity modifier effect on the final armor class.
  - **Stl.dis** indicates whether you have a stealth check disadvantage.
  - **Str** indicates the minimum strength value you need to wear this armor without speed penalty.
  - **Shield** allows adding your shield's AC to the final armor class.
    The checkbox indicates that you're holding the shield, and it's armor class is being applied.
    
- **Hit dice** shows how many hit dices you have left.
  - **Used** is for keeping track of how many hit dices you've used so far.
  - **Base** is the maximum number of hit dices you can have.
    By default, it's equal to your *level*.
  - **Dice** stores info of which hit dice your class uses.]
    By default, it's calculated based on your *class*.
  If you decide to multiclass, you can scrap all contents of this entry and fill it yourself.
  
- **Initiative** is a bonus to your initiative rolls.
  - **Prof** allows adding your proficiency bonus to the initiative.
    Checking the left checkbox adds a single proficiency bonus,
    checking the right checkbox adds half of the proficiency bonus,
    and checking both adds a double proficiency bonus.
  - **Misc** allows you to add a modifier to your initiative.
  - **Extra** allows adding a stat modifier to your initiative.

- **Prof** is your proficiency bonus.
  At the moment, it is not calculated automatically, so you'll have to set it yourself.
  
- **Str, Dex, Con, etc.** shows your stats and stat modifiers.
  - **Base** is the stat itself, enter it manually.
  - **Save** is the stat modifier used for saving throws.
  - **Prof** allows adding a proficiency bonus and an arbitrary modifier to the save throws.

- **Skill table on the right** shows stat modifiers for skill checks,
  allows adding notes to any skill
  (for example, to indicate experteese with some particular topic, like stoneworks for dwarfs),
  and indicating proficiency and experteese with a skill.
  Checking the left checkbox indicates proficiency with a skill,
  checking the right checkbox indicates half proficiency with a skill,
  and checking both indicates experteese with a skill.
  The value after checkboxes is an arbitrary modifier that you can set for a skill.

## Features and notes

This is just a text section for keeping track of any notes you want.
You're free to re-arrange it to your liking.

## Spells and actions

## Weapons

## Inventory

## Having multiple characters on one sheet

## Formulas

## Aux sheet
