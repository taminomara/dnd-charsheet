# Character stats

The section contains main character attributes.

Fill in your **class**, **level**, **stats** and **proficiencies**,
the rest is calculated for you.

<img alt="Base stats" src="https://user-images.githubusercontent.com/81165235/176145013-fbf8d632-1a47-4fd2-98fd-1003e09715b2.png">

## Detailed description of all cells

- **Name, race, alignment, age, appearance, languages** are just text cells that you may fill with anything you like.

- **Class** is a dropdown with standard classes. If you're playing a custom class,
  add it [at the *Aux* sheet](./08_aux_sheet_and_formulas.md).

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

----

[◁ Previous](./01_intro.md) • [Home](../README.md) • [Next ▷](./03_features_and_notes.md)
