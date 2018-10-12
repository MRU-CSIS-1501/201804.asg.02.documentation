# Some Guidance for the DnD Challenge

Estimated Reading Time: **9 minutes**

## A suggestion: _start with DndRulesHelper_

I'd suggest working on the TODOs in the DndRulesHelper file first for a few reasons:

- you'll pass most of the tests that way - which gives you a higher mark on the automated tests portion of this challenge's total grade
- the DndDamageCalculator can't be completed fully until the DndRulesHlper TODOs are done
- each method in DndRulesHelper is focused on doing just one small thing, which makes them easier to complete

## Easier methods

In the DndRulesHelper file, these methods are easier to do:

- `damageTypeFor`
- `abilityModifierFor`
- `hasProficiencyIn`
- `proficiencyBonusForLevel`
- `minDamageFrom`

In the DndDamageCalculator file, these methods are easier to do:

- `isAllowableCharacterClass`
- `ordinalFromNumber`

## Use methods that are already completed

There is an expectation in this challenge that you will have at least looked through the documentation in both source files - you don't necessarily need to know _how_ every method works, but you should know _what_ they do.

Many of the TODO methods use other methods that have already been completed - which makes coding these TODOs **much** easier.

There are the methods that **don't** use other pre-built methods:

- `abilityModifierFor`
- `proficiencyBonusForLevel`
- `minDamageFrom`
- `ordinalFromNumber`
- `isAllowableCharacterClass`

## A simple glossary for this challenge

If you don't have any experience in D&D, there are a lot of words being tossed at you in this challenge which might cause some head-scratching. Here's a glossary that might help a bit.

- **Attack Roll Bonus**: a number that measures how good a character is at hitting things with a given weapon. High numbers are better. A negative number is bad.
- **Damage**: a range of numbers representing how much "ow" a character can do with a weapon.
- **Proficient**: if a character is _proficient_ in a certain weapon, it means they know how to use it properly. If you give a big ole sword to a farmer off the street and ask them to fight with it, chances are they won't have a clue how to use it properly - because they're not proficient in it.
- **Proficiency Bonus**: a number that measures how good a character is at hitting things - _with a weapon they're proficient in_. You can add this bonus to your attack roll bonus _if you're proficient in the weapon you're attacking with_.
- **STR**: a number representing the raw, brute power a character has. (This is one of the two **ability scores** used in this challenge.) Characters with high strength have a better chance of hitting things - and will do more damage when they _do_ hit. (Think Conan the Barbarian vs. Eugene from Accounting.)
- **DEX**: a number representing how fast and nimble a character is with their hands. (This is the other **ability score** used in this challenge.) Characters with high dexterity have a better chance to hit things with weapons that require some speed and finesse - even if they have low strength. (Think any of the hobbits in the Lord of the Rings movies.)
- **Ability Score Modifier**: a number that measures how good a character's ability is. Higher numbers are better. Negative numbers suck.
- **Simple Weapon**: a weapon that doesn't require any special training to use. (Most people can figure out how to whack something with a club, or stick the business end of a dagger into somebody.)
- **Martial Weapon**: a weapon that is tricky to use in some way (maybe it's oddly balanced, or you have to swing it a certain way to be effective). If you don't have training in these tricky weapons, you're not going to be very good at hitting things with them.
- **Finesse Weapon**: a weapon that can benefit from being wielded with brute strength **or** with some speed and agility.
- **Piercing Damage**: damage that comes through pointy objects going into soft things.
- **Bludgeoning Damage**: damage that comes through heavy, blunt objects smashing into soft things. And hard things.
- **Slashing Damage**: damage that comes from blade-y objects slicing through soft things.

## An illustrative story, followed by example calculations

Let's do some calculations together; lend me your imagination for a moment...

_Our scene opens, as many adventures do, in a tavern. It's a quiet night inside, most potential customers staying away due to the miserable weather outside._

_In a shadowy corner sits a stained and battered table by a roaring fire. Seated around the table are a group of 4 rough-looking hombres._

_One, a **very** large and **very** heavily-muscled woman, is engaged in a "friendly" arm-wrestling match with a profusely-sweating stocky man whose chainmail armour is reflecting the flames of the fire. (It is hard to tell whether he is sweating from the fire's heat, or from the exertion of the contest...but the mocking grin on the woman's face would seem to indicate the latter.)_

_A slender person of indeterminate gender sits with their feet propped up on the table. They point at the fire periodically; each time this happens, a sharp cracking sound is followed by a shower of sparks that fly up and then onto the beer-soaked floor._

_A rat-faced man dressed in black is at the bar, arguing heatedly with the bartender. He punctuates every sentence with a wave of a wicked-looking dagger held loosely in his hands._

_Our scene is interrupted as a huge crash fills the room - the door to the tavern has just **blown** off its hinges and a wave of dark shapes rush into the bar and make a beeline for our players._

> **The Players**
>
> **Bel** (Level 4 Fighter)
>
> - Weapon: maul
> - STR: 18
> - DEX: 14
> - Bel enjoys fighting. A lot. Mostly because she likes to hurt thngs. A lot.
>
> **Dureth** (Level 3 Cleric)
>
> - Weapon: rapier
> - STR: 16
> - DEX: 13
> - Dureth didn't bring his own weapon to the tavern - he thought this was going to be his night off - so is forced to grab an old rapier on display over the fireplace.
>
> **Shanahay the Spark** (Level 6 Wizard)
>
> - Weapon: sickle
> - STR: 7
> - DEX: 10
> - Shanahay finds it amusing to set people on fire. But in a pinch, a little bit of sickle-work will do.
>
> **Zethix** (Level 4 Rogue)
>
> - Weapon: dagger
> - STR: 9
> - DEX: 18
> - Zethix considers a back incomplete unless it has a dagger firmly planted in it.

Let's imagine what would happen to each player if they decided to use their weapon to take a whack at a foe.

### Scenario 1: Bel whacks something with her maul

- Bel is level 4, so her proficiency bonus is +2. (Character Advancement table on pg. 10)
- Bel is a fighter, so she is proficient in both simple and martial weapons. (Classes table on pg. 20)
- The maul is a martial weapon that does 2d6 (2 to 12) points of bludgeoning damage (Weapons table on pg. 46).
- Bel has a STR of 18, giving her a strength ability modifier of +4. (Ability Scores and Modifiers table on pg. 7)
- Bel has a DEX of 14, giving her a dexterity ability modifier of +2.
- To calculate her attack roll bonus, she would add her proficiency bonus of +2 (since she's proficient with the maul) with her strength ability modifier of +4 for a total attack roll bonus of +6. (Attack Rolls section, pg. 73)
- To calculate the damage done by an attack, she would add her strength ability modifier of +4 to the 2 to 12 damage the maul normally does. This gives a range of 6 to 16 damage. (Damage Rolls section, second paragraph, pg. 74)

### Scenario 2: Dureth tries to skewer with a borrowed rapier

- Dureth is level 3, so his proficiency bonus is +2.
- Dureth is a cleric, so is proficient in simple weapons - but not martial weapons. This will be important.
- The rapier is a martial weapon that does 1d8 (1 to 8) points of piercing damage. It's also a **finesse** weapon - this, too, will be important.
- Dureth has a STR of 16, giving him a strength ability modifier of +3.
- Dureth has a DEX of 13, giving him a dexterity ability modifier of +1.
- To calculate his attack roll bonus, he gets to choose the higher of his ability modifiers because the rapier is a finesse weapon. In this case, it's his strength modifier of +3. He does **not** get to add his proficiency bonus, because he is not proficient in the rapier, so his total attack roll bonus is +3.
- To calculate the damage done by an attack, he would add his strength ability modifier of +3 to the 1 to 8 damage the rapier normally does. This gives a range of 4 to 11 damage.

### Scenario 3: Shanahay slices and dices with his sickle

- Shanahay is level 6, so their proficiency bonus is +3.
- Shanahay is a wizard, so is only proficient in certain weapons - and the sickle isn't one of them.
- The sickle is a simple weapon that does 1d4 (1 to 4) points of slashing damage.
- Shanahay has a STR of 7, giving them a strength ability modifier of -2.
- Shanahay has a DEX of 10, giving them a dexterity ability modifier of +0.
- To calculate their attack roll bonus, they just use their strength modifier of -2. They don't get to add their proficiency bonus because they're not proficient with the sickle. So their total attack roll bonus is a whopping -2.
- To calculate the damage, they would add their strength ability modifier of -2 to the 1 to 4 damage the sickle normally does. This gives a range of 0 to 2. (It's not -1 to 2, because you can never do negative damage!)
- _Note: It's obvious that Shanahay shouldn't really be mixing it up in this fight!_

### Scenario 3: Zethix goes stabby-stabby with his dagger

- Zethix is level 4, so his proficiency bonus is +2.
- Zethix is a rogue, so is only proficient in simple weapons (and others as well - but that's not important here).
- The dagger is a simple weapon that does 1d4 (1 to 4) points of piercing damage. It's also a **finesse** weapon - this will be important.
- Zethix has a STR of 9, giving him a strength ability modifier of -1.
- Zethix has a DEX of 18, giving him a dexterity ability modifier of +4.
- To calculate his attack roll bonus, he would add his proficiency bonus of +2 to the better of his two ability modifiers (since he's using a finesse weapon). That would obviously be the +4, so his total attack roll bonus would be +6.
- To calculate the damage, he would add his dexterity ability modifier (thanks to the finesse) of +4 to the 1 to 4 damage the dagger normally does. This gives a range of 5 to 8.
