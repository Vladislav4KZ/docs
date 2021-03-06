****************
Bot Usage
****************

The YaPB User Menu (yb menu)
================================

Main Menu
-----------------

Pressing the "=" key in game a menu with the following options should appear on your screen

.. figure:: images/main_menu.png
    :align: center

    This is the YaPB user menu
    
1. **Control Bots** - A menu that adds or removes bots from the game.
2. **Features** - A menu that configures the type of weapons used by bots, opens the waypoints menu, toggles debug mode and controls bots commands.
3. **Fill Server** - A menu that fills the server with bots with the specified parameters.
4. **End Round** - Kills all bots for the end of round.

Bots Control Menu
---------------------

.. figure:: images/bots_control_menu.png
    :align: center

    Bots Control Menu
    
1. **Add a Bot, Quick** - This does what it says. It quickly adds a Bot giving him a random name, team, difficulty and model. Difficulty will be chosen randomly between your yb_difficulty_min/yb_difficulty_max values specified in yapb.cfg.
2. **Add a Bot, Specified** - Allows you specify all things (except name) for adding a single Bot.

.. figure:: images/bots_difficulty_level.png
    :align: center

    This lets You choose a difficulty for the specific Bot.
    
.. figure:: images/bots_personality_menu.png
    :align: center

    This lets You choose a personality for the specific Bot.

.. figure:: images/select_team_menu.png
    :align: center

    This lets You choose a team for the specific Bot.

.. figure:: images/ct_class_select.png
    :align: center

    This lets You choose a class for the specific Bot. (for CT Team)

.. figure:: images/t_class_select.png
    :align: center

    This lets You choose a class for the specific Bot. (for T Team)
    
3. **Remove Random Bot** - removes a random bot.
4. **Remove All Bots** - removes all bots from the server.
5. **Remove Bot Menu** - A menu that allows you to remove a bot from the server specified in the list.


Bots Features Menu
-----------------------

.. figure:: images/bots_features_menu.png
    :align: center

    Bots Features Menu
    
1. **Weapon Mode Menu** - A menu that configures the type of weapons used by bots.

.. figure:: images/bots_weapon_mode.png
    :align: center

    Bots Weapon Mode Menu

2. **Waypoint Menu** - Opens the waypoint menu.
3. **Select Personality** - Adds a bot with the currently set difficulty with personality setting.
4. **Toggle Debug Mode** - Enables or disables debug mode.
5. **Command Menu** - Opens the bot command menu.

.. figure:: images/bot_commandmenu.png
    :align: center

    Bot Command Menu
    
1. **Make Double Jump** - Forces the nearest teammate bot to crouch next to you to make double jump.
2. **Finish Double Jump** - Releases the bot after the first command, it must get up and go about his business.
3. **Drop the C4 Bomb** - Forces the bot carrying the bomb to drop it at you.
4. **Drop the Weapon** - Makes the teammate bot throw a weapon at you.


Waypoint Menu
------------------

.. figure:: images/waypoint_menu_page1.png
    :align: center

    Waypoint Editor Menu (Page 1)
    
1. **Show/Hide waypoints** - Show or hide the display of waypoints.
2. **Cache waypoint** - Cache waypoint for future use.
3. **Create path** - Opens the menu for creating path connections.
4. **Delete path** - Removes the path from selected waypoint.
5. **Add waypoint** - Opens the menu for selecting the type for adding waypoint.
6. **Delete waypoint** - Removes the waypoint you are standing on.
7. **Set Autopath Distance** - Opens the autopath distance setting menu.
8. **Set Radius** - Opens the waypoint radius setting menu.
9. **Next...** - Goes to the second page of the waypoint menu.

.. figure:: images/waypoint_menu_page2.png
    :align: center

    Waypoint Editor Menu (Page 2)

1. **Waypoint stats** - Shows statistics on the number and types of waypoints on the map in the console.
2. **Autowaypoint on/off** - Enables or disables automatic waypoint placement.
3. **Set flags** - Opens the menu for selecting flags for a waypoint.
4. **Save waypoints** - Saves waypoints with path integrity check.
5. **Save without checking** - Saves waypoints without checking (because of this, there may be problems with the behavior of bots).
6. **Load waypoints** - Loads waypoints from a file.
7. **Check waypoints** - Checks waypoints for errors.
8. **Noclip cheat on/off** - Enables or disables noclip cheat.
9. **Previous...** - Goes to the first page of the waypoint menu.


YaPB console commands Summary
==================================

The following main YaPB commands are available (note these ARE case sensitive):
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb add``                | Adds specific bot into the game. (see below)                                                                                   |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb kick``               | Kicks off the random or specified bot from the game. (see below)                                                               |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb removebots``         | Kicks all the bots from the game. Also available via alias ``yb kickall``                                                      |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb kill``               | Kills the specified team or all the bots. (see below)                                                                          |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb fill``               | Fills the server (add bots) with specified parameters. (see below)                                                             |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb vote``               | Forces all the bots to vote to specified map.                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb weapons``            | Sets the bots weapon mode to use. (see below)                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb menu``               | Opens the main bot menu.                                                                                                       |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb version``            | Displays version information about bot build.                                                                                  |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb list``               | Lists the bots currently playing on server.                                                                                    |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+
   | ``yb cvars``              | Displays all the cvars with their descriptions.                                                                                |
   +---------------------------+--------------------------------------------------------------------------------------------------------------------------------+


yb add
---------------

To add a specific bot to the game, with nickname: John Smith, difficulty 2. Average, personality 4. Careful, team: CT, team class: SAS, you should type in console ``yb add 2 4 2 3 "John Smith"``

Correct format for the ``yb add`` command is ``yb add [difficulty][personality][team][model][name]``. All bot values ​​are selected by numbers (except the bot name).

yb kick
---------------

Type in console ``yb kick`` command to remove the random bot.

If you want to remove the bot from the specified team, you should type in the console ``yb kick t`` to kick a bot from Terrorists team, and ``yb kick ct`` to kick a bot from Counter-Terrorists team.

yb kill
---------------

The ``yb kill`` command kills all the bots. To kill a specific team, such as terrorists you should type in console ``yb kill t`` command. For Counter-Terrorists the command are ``yb kill ct``

yb fill
---------------

To fill the server with random bots type in console ``yb fillserver``.

If you want to fill the server with specific bots, for example: Team: Terrorists, Count: 5, Difficulty: 3. Normal, Personality: 2. Aggressive, you should type in console the follow command ``yb fill 1 5 3 2``.

Correct format for the ``yb fill`` command is ``yb fill [team][count][difficulty][personality]``.

yb weapons
---------------

To force the bot to use only a certain type of weapon, for example, shotguns, you should type in console the ``yb weapons shotgun`` command.

Allowed values: ``knife|pistol|shotgun|smg|rifle|sniper|standard``.

Standard means that bots will use all weapons.

Adding bots to the game
============================

Select ``1. Add a Bot, Quick`` from the bot control menu to add a bot with random stats (name, difficulty, personality etc.)
Select ``2. Add a Bot, Specified`` from the bot control menu to add a bot with manually specified stats.

Or type in console ``yb_quota x`` where X is amount of adding bots.


Selecting the bot language
=============================

You must open the file ``yapb.cfg`` in the folder ``addons/yapb/conf`` and change the value of yb_language cvar to the next available one.

#. ``en`` - English Language
#. ``ru`` - Russian Language
#. ``de`` - Deutsch Language
#. ``chs`` - Chinese Language

For example, write in the config ``yb_language ru`` for Russian Language.