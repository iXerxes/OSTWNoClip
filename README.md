# OSTW NoClip Module
## An advanced, but relatively light-weight NoClip module for the Overwatch Workshop.

### What is it?

Originally created as a normal [Workshop mode](https://workshop.codes/VETFH), and then turned into an [OSTW](https://github.com/ItsDeltin/Overwatch-Script-To-Workshop) module.

NoClip allows you to start and stop flying on command, but also without the restrictions of clipping into or against the environment.

This script is designed to be a module and aims to be a lightweight package so that it can fit into any project with as few side affects and disruptions as possible.

> If you're just wanting a way to view the map without including it in your project, the script can work fully standalone, so you're welcome to try it out that way too :)

___

### Features
- Allow/disallow specific players to use NoClip.
- Show name tags of the positions of players using NoClip
- Very easy to set/change the activation method. (Keybind)
- Fly in the direction your're facing, and pass through walls into out-of-bounds areas.
- As you'd expect, you go back to regular form once you exit NoClip, continuing from that position.
- Seamlessly switch in and out of NoClip from your current position.
- Allows you to change the global properties such as permissions, name-tag visibility, default speed, boost speed and camera smoothing.
- **Easy to configure** - Everything is configurable using the Workshop settings menu.

___

### OSTW API
A few macros have been created to make it a little easier to interact with as an OSTW module:

- <b>HasNoClipAccess</b> - Check if the specified player has access to NoClip; __returns Boolean__.<br>
`Boolean HasNoClipAccess(Player player)`
  - `player`: The player you want to check.

  Example: `If (HasNoClipAccess(EventPlayer())) { ... }`

  <br>

- <b>IsUsingNoClip</b> - Check if the specified player is currently using NoClip; __returns Boolean__.<br>
`Boolean IsUsingNoClip(Player player)`
  - `player`: The player you want to check.

  Example: `If (IsUsingNoClip(EventPlayer())) { ... }`

  <br>

- <b>NoClipPosition</b> - Get the position of the specified player's NoClip camera; __returns Vector__.<br>
`Vector NoClipPosition(Player player)`
  - `player`: The player to get the NoClip position of.

  Example: `NoClipPosition(EventPlayer());`

  <br>

- <b>SetNoClipAccess</b> - Set whether or not the specified player has access to use NoClip; __returns void__.<br>
`void SetNoClipAccess(Player player, Boolean hasAccess)`
  - `player`: The player to set access for.
  - `hasAccess`: Whether or not the player has access.

  Example: `SetNoClipAccess(EventPlayer(), false));`

  <br>

- <b>ToggleNoClip</b> - Toggle the current NoClip state for a player. This is basically just pressing the toggle button *for* the player; __returns void__.<br>
`void ToggleNoClip(Player player)`
  - `player`: The player to toggle the NoClip state of.

  Example: `ToggleNoClip(EventPlayer()));`

___

### Controls & Properties:
- Controls:
	- Toggle NoClip (configurable): Q/Ultimate
	- Up: Space/Jump
	- Down: Ctrl/Crouch
	- Shift/Ability 2: Speed Boost
	- Forwards
	- Backwards
	- Left
	- Right
<br><br>
- Default Properties (All Configurable)
	- Access - Everyone has the ability to use NoClip
	- Name-Tag Visibility - Everyone can see the position of a NoClip user.
	- Normal flight speed (Meters/s): 10
	- Boosted flight speed (Meters/s): 20
	- Camera Smoothing: 25