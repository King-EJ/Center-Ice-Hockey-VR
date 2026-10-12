# Center-Ice-Hockey-VR
VR Mod for Center Ice Hockey (just trying something it will be awhile before i get back to this)

CENTER ICE HOCKEY VR  -  VR mod for "Center Ice Hockey" (Unity 2022.3, IL2CPP)
=============================================================================

Version 0.1.2 (test build).

WHAT IT DOES
------------
* Stereo VR through OpenXR (SteamVR, Meta/Oculus, Virtual Desktop, WMR...).
* Three VR views (hold Y to switch):
    GameCamera - you sit where the game's TV camera is and move with it, horizon kept level.
                 Pick Side / Classic / Overhead / Action in the game's own settings as usual.
    Seat       - a fixed seat where the camera was (it does not pan with the play).
                 Click both sticks to move the seat to where the game camera is now.
    Skater     - (experimental) first person in the skater you control. "Up" on the left
                 stick skates where you look, the right stick turns.
* In GameCamera view the HUD screen lines up with the game camera's view, so the player
  markers and arrows sit on the players.
* The VR controllers act as an Xbox gamepad for the game's own controls and menus.
* Menus are on a screen floating in front of you.

INSTALL
-------
1. Copy the files from this zip into the game folder).
2. Start SteamVR (or your OpenXR runtime), then start the game.


CONTROLS (gamepad layout)
-------------------------
Left stick ............... left stick       Right stick ........ right stick (Skater view: turn)
A ........................ A                B .................. B
X (tap) .................. X                Y (tap) ............ Y
Hold Y (about 1 s) ....... switch VR view GameCamera -> Seat -> Skater
Left / right grip ........ LB / RB          Left / right trigger LT / RT
Left / right stick click . L3 / R3          Both stick clicks .. re-centre
X + Y together ........... Start (pause)    Hold X ............. Back / View
In menus the right stick is also the d-pad.
Everything is in BepInEx\config\centericehockey.vr.cfg ([Controls] = gamepad buttons).

MENUS:                  use the sticks like a gamepad, or point your right hand at the menu screen
                        (blue laser) and pull the trigger.
IN-GAME SETTINGS MENU:  hold Y + left stick click for 1.7 s (view, world scale, camera, HUD...).
HAND ADJUST:            hold Y + right stick click for 1.5 s.

USEFUL SETTINGS
---------------
[View] ViewMode = GameCamera / Seat / Skater
[View] GameCameraPullBack = 0       (metres behind the TV camera - more of the rink in view)
[View] GameCameraRaise = 0          (metres up / down)
[Camera] IceReflection = PerEye     (the mirror ice: PerEye / Off / Game - if you still see a glare, use Off)
[Camera] WorldScale = 1             (try 10-20: the rink becomes a table-top model in front of you)
[UI] AlignHudWithGameCamera = true  (false = floating HUD screen instead)
[UI] AlignedHudDistance = 3
[General] MovementDirection = Game / Head / OffHand   (which way "up" on the stick skates)
[General] MovementYawFromGame = true                  (Skater view skates the wrong way? set false)


Uses Astien's OpenXR bridge (see BepInEx\plugins\CIVR\LICENSES). Free, non-commercial.

