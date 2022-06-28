# DnD charsheet

This is a character sheet template made in google sheets, powerful yet flexible.

Current release: [v0.2] (see an [example], my lvl5 artificer Nissa). Make a copy and fill in for your character!

*Note: this is an alpha release. I'm fairly new to DnD, so some functionality may be missing.*
*Please [report any bugs and feature requests] to this repo.*

[v0.2]: https://docs.google.com/spreadsheets/d/1CUvzUhWbFLaV_pfz20NMdJCa-dJ7vRbiKOHLn0vZgXY/edit?usp=sharing
[example]: https://docs.google.com/spreadsheets/d/1eInNnRA1s2wx3-wW0L9C2Dzz4jeJA5OS3K8GeLl9hyA/edit?usp=sharing
[report any bugs and feature requests]: https://github.com/taminomara/dnd-charsheet/issues

----

<img width="1117" alt="image" src="https://user-images.githubusercontent.com/81165235/174246117-2a1cd3d0-c99a-4c77-a5a8-0c1ccc2fb1c4.png">

----

## Documentation

There are five sections in the carsheet:

- character stats,
- features and notes,
- spells and actions,
- weapons,
- inventory.

You can move them vertically, copy them, or rearrange them.
You can't move them horizontally.
Since sections contain hidden formulas in columns `C:P`,
you can't copy or move just a part of a section.

**When you copy a section,** it will search for the nearest
character stats section above itself, and use stats from there.
So you can have multiple characters on one sheet
by copying character stats section
and placing additional sections after it.

<img alt="Copying sections" src="https://user-images.githubusercontent.com/81165235/175997156-836dfc8b-8538-429d-9003-a94f4a071b0a.gif" width="400">

**When you need to remove a section,**
select its rows and delete them.
This will clear conditional formatting and data validation.

<img alt="Deleting sections" src="https://user-images.githubusercontent.com/81165235/175997620-4f9f3cad-de86-4209-8fdd-95edb0634251.gif" width="400">

**When you need to add new rows to tables,**
use the "Insert > Rows" menu to insert a row,
then fill the new row with formulas
by selecting a previous row and dragging the selection down
by its bottom-right corner.

<img alt="Adding rows" src="https://user-images.githubusercontent.com/81165235/175994987-c01722a7-50a7-4c70-b689-bcf6d4adbc45.gif" width="400">

**When you configure proficiency,**
and you see two checkboxes,
enabling the left checkbox adds a single proficiency bonus,
enabling the right checkbox adds half of the proficiency bonus,
and enabling both adds a double proficiency bonus.

<img alt="Configuring proficiency" src="https://user-images.githubusercontent.com/81165235/175998352-a2c96532-cbaf-4282-9ef2-81658e86b13c.gif" width="400">

**When you configure stats,**
there are usually unlabeled cells
with grey numbers near them
that allow adding misc bonuses.

<img alt="Misc bonuses" src="https://user-images.githubusercontent.com/81165235/176000464-ea463c5a-fde9-46ec-9644-e1e7bfc5ed1e.png" width="400">

### Character stats

The section contains main character characteristics.

Fill in your **class**, **level**, **stats** and **proficiencies**,
the rest is calculated for you.

<!-- <img alt="Base stats" src="https://user-images.githubusercontent.com/81165235/176145013-fbf8d632-1a47-4fd2-98fd-1003e09715b2.png"> -->

<details>
  <summary>Detailed description of all cells</summary>

  <blockquote>

  - **Name, race, alignment, age, appearance, languages** are just text cells that you may fill with anything you like.

  - **Class** is a dropdown with standard classes. If you're playing a custom class, add it [at the *Aux* sheet](#aux-sheet).

  - **Inspiration** is a checkbox for tracking if you have one.

  - **HP** shows your HP.
    - **Base** is your maximum HP.
      By default, it is calculated as an average dice roll for your class per level.
      If you want to throw dices instead, scrap the formula and fill the cell with a custom value.
    - **Dmg** is for keeping track of all damages and heals.
      When you take damage, subtract HPs from this cell value.
      When you heal, add HPs to this cell value.
      The value in this cell should always stay negative.
    - **Temp** is for keeping track of temporary HPs given to you by spells.
      When you're assigned temp HPs, save them to this cell.
      When you're taking damage, subtract HPs from this cell first,
      then subtract anything that's left from the *Dmg* cell.
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
    - **Dex <** limits your dexterity modifier effect on the final armor class.
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
    - **Misc** allows you to add a modifier to your initiative.
    - **Extra** allows adding a stat modifier to your initiative.

  - **Prof** is your proficiency bonus.
    It is calculated automatically based on your level.

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

  </blockquote>
</details>

### Features and notes

This is just a text section for keeping track of any notes you want.
You're free to re-arrange it to your liking.

### Spells and actions

This is a table with all
actions, spells, skills, consumable items, etc.
that you can take in or outside of a fight.

Choose your **spellcasting ability**
to calculate **SA** (spell attack bonus)
and **DC** (difficulty class for your spell's save rolls).

<details>
  <summary>Detailed description of all columns</summary>

  <blockquote>

  - **Prepared** column contains checkboxes which indicate
    that the spell or action is available,
    i.e prepared, learned, stored in an inventory.

  - **LR, SR** column shows how much uses of a spell
    you regain after a long or a short rest.

  - **Uses remaining** column is for tracking used items
    and spells. You can fill it with checkboxes
    and disable a checkbox after you use a spell,
    or you can merge its cells and put a number in them.
  
  - **Spell/Action** column contains name of the spell.
    You can add a cell note with a description of what
    the spell does, so you don't have to google it in game.
    
    <img alt="Cell note" src="https://user-images.githubusercontent.com/81165235/176010135-85f91181-ffe9-45ef-bd40-23677ba5ee43.png" width="400">

  The rest of the columns are used at your discretion.
  
  </blockquote>
</details>

### Weapons
  
This section contains weapons.
**AB** (attack bonus) and **damage**
are calculated using columns on the right.
  
<details>
  <summary>Detailed description of all columns</summary>

  <blockquote>

  - **Armed** is a checkbox which shows that the weapon is loaded and ready to be used.

  - **Range** is a text column with weapon's range.

  - **AB/Save** contains weapon's attack bonus
    (or difficulty check for weapons that require saving throw)
    is calculated automatically.
  
  - **Damage** is also calculated automatically.
  
  - **Dmg Type** is a dropdown with weapon's damage type.

  - **Weapon** is a name of a weapon.

  - **Ranged type** is a dropdown showing if the weapon is melee or ranged.

  - **Handed type** is a dropdown showing if the weapon is one- or two-handed.

  - **Ability** is a dropdown indicating which ability is used to use a weapon.
    Usually it's *Str* or *Dex*.

  - **Proficiency** indicates if you're proficient with a weapon.

  - **Damage dice** is a dice spec that you roll to deal damage,
    i.e. `4d4` or `2d8`.

  - **Attack bonus** is a misc bonus to *AB/save*.

  - **Damage bonus** is a misc bonus to *damage*.

  - **Add ability mod to damage** adds your *ability* modifier to weapon's damage.
    Enabled by default because most basic weapons need this.
  
  </blockquote>
</details>

### Inventory

### Scripts

### Aux sheet

### Formulas
