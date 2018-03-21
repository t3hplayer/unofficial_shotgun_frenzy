Unofficial SF 1.4 Patch, Version 6, alpha 1
(Note: This includes both the unofficial patch
AND the unofficial weapons tweak, which were
originally separate items)

This is an *unofficial* update to Shotgun Frenzy v1.4.
*UNOFFICIAL*, meaning, I am not the original author
of Shotgun Frenzy.
This update is a modification of the source originally
included in sfrenzy14.pk3.

The modification originally set out to address several
known exploits which users are exploiting
to get, essentially, infinite money. Since,
this project had done weapon rebalancing, enemy
rebalancing, and a number of other changes. There
are a number of new server side console settings
that are used.

New console variables:

sf_startcash (Sets each player's starting cash. Capped at 20000)
sf_teamcash  (Sets the team's starting cash. Only for SF maps)
sf_gamelength (Sets the length of time before the map starts the guardian wave)
sf_creditcorrection (Described below)
sf_percentfast (Described below)

sf_creditcorrection is to discourage users hopping between spectating / playing,
in the hopes of gaining additional money (which is possible since the game
recalculates a player's cash any time he joins, and the amount given increases
with level time). sf_creditcorrection can be used to increase or reduce the
value by which starting cash increases with level time.
For example, something like

set sf_creditcorrection -8

will cause the cash to increase less with time than it does in the original
SF 1.4. Sensible values are from -10 (no credit bonus) to +infinity,
though the sensibility of the latter is debatable. Negative values
reduce the credit bonus for new players / people joining from spec.
Positive values increase this bonus.

sf_percentfast results in some percentage of the monsters randomly being "fast."
These monsters move 1.5x their normal speed.  Default is 0. Only works
when > 2 players

How to run:

Add this file to the Zandronum command line *after* the original SF files. Example:

./zandronum -iwad doom2.wad -file skulltag_actors_1-1-1.pk3 -file skulltag_data_126.pk3 -file sfrenzy14.pk3 -file sfrenzy14_core.pk3 -file sf14unofficialpatch5.pk3

Things fixed (that I remember):

Old versions:
  Credit / upgrade costs listed in menu now match actual costs (some were mismatched before)
  Cannot recycle dualshot razor when you don't have it (people love to exploit this one)
  Hopefully impossible to use the mech weapons while not in the mech (less common)
  BFG and Flamer now have upgrades
  BFG behaves like a real BFG when upgraded
  Flamer penetrates and is much more powerful when upgraded
  No longer possible to block the elevators / doors in SF maps
  Added Spider-based enemies (SpiderAnnihilator and Arachnotron) to spawn waves
  Beefed up Juggernaughts (hopefully enough this time -- they were still way too weak in the last one)

UP7a1:
  Turrets laid by a player are now automatically removed upon spec / disconnect
  Elevators in SF maps now go to correct height

contact: t3hdoom@gmx.com
