# Unofficial Shotgun Frenzy Update

This is an *unofficial* update / patch for Shotgun Frenzy v1.4. Over time, users have found various exploits, imbalances, and other things to exploit in Shotgun Frenzy v1.4. This *unofficial* update seeks to address these various issues.

Shotgun Frenzy is a cooperative Doom 2 mod that pits players against a bunch of huge waves of enemies. For more information, check the [v1.4 release thread on the Zandronum forums](https://zandronum.com/forum/viewtopic.php?t=479).

There's also a [rarely-updated post about this unofficial patch on the Zandronum forums](https://zandronum.com/forum/viewtopic.php?t=4274).

## Instructions

Load the sf14unofficialpatch pk3 file *after* the normal Shotgun Frenzy stuff. Example command line:

    ./zandronum-server -iwad doom2.wad -file skulltag_actors_1-1-1.pk3 -file skulltag_data_126.pk3  -file sfrenzy14.pk3 -file sfrenzy14_core.pk3 -file sf14unofficialpatch5.pk3

There are a few new console variables that the server can set to control various aspects of the game. They are:

    sf_startcash
Sets each player's starting cash. For example, if I wanted my server to have players start with 2000 instead of 2500 cash, I'd simply issue "set sf_startcash 2000" in my server console.

    sf_teamcash
Similar to sf_startcash, except this sets the team's starting cash. Only relevant for SF maps.

    sf_gamelength
Sets the length of the game up to the two-minute warning for the Guardian Wave. So, if you set this to 33 minutes, the Guardian Wave will happen at the 35 minute mark.

    sf_creditcorrection
This one is a little tricky. Internally, the game alters the amount of starting cash a player gets based on how much time has elapsed. That way, players get more cash when they join later in the game. The idea is that this helps late-joining players stay competitive, since they haven't had as long to earn cash. In reality, though, some players find that too much cash is earned over time, and they like to reduce this payout. That's what this variable is for. Set it to a negative value if you want to cash to increase more slowly over time, and use a positive value for the opposite effect. In my experience, -8 is a pretty good setting.

    sf_percentfast
This one is fun. This sets the percentage of monsters which spawn with super fast running speed (from 0 to 100). Only triggers when there are at least 3 players. Often entertaining results.
