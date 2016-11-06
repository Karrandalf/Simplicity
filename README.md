# A Minimalist Dual Modifier DotA 2 Keyboard Setup

### What is this?

OLite is a custom keyboard setup for Dota 2 that makes use of two modifier keys for Windows users. SteamOS and other linux users already enjoy keyboard setups that utilize both their super key and alt as modifiers, whereas Windows users can only use one modifier. This is because Microsoft's Windows key shortcuts cannot be disabled entirely wihtout disabling the Windows key itself. To ensure that the user does not experience any of the shortcuts during gameplay while using the second modifier, a very short ahk key script runs in the background to block the Windows key shortcuts from the os while Dota 2 is the active window. The windows modifier is then bound to LAlt as many windows users choose to disable the windows key for all games. The original alt modifier is then rebound in-game to the spacebar. This gives you two modifiers: LAlt and Space.

I believe that no player should have an in-game advantage because of their operating system. OLite gives the same opportunities that SteamOS and linux users have by default to windows players by enabling a second modifier.

### How to set it up?
#To Install:

1. Place OLite.exe in your StartUp folder (I have provided a shortcut).
   You can use the .ahk instead if you have installed AutoHotKey. https://autohotkey.com/

2. Place the "Game" folder inside of "Steam\steamapps\common\dota 2 beta" and overwrite.

3. Place the "570" folder inside of "Steam\userdata\ [Your 9 digit Steam ID here] " and overwrite.

4. Restart your computer. OLite.exe will run in the background but will not be active unless
   you have dota2 running and are "alt-tabbed" into it.

5. launch DotA 2 and customize to your liking
####Note: LAlt binds the LAlt modifier but it will read "WINDOWS" in-game. RAlt binds the SPACE modifier but it will read "ALT" in-game.

### How to uninstall?

1. Just delete the files you pasted in the `Game`, `570`, and `StartUp` folder.

2. Set your keybinds back the way you want them

3. Enable double-tap for self-cast in the dota 2 options by raising the timeout to something around 0.5

*Note: Double tap selfcast is intentionally disabled to prevent miscasts*


### Frequently Asked Questions

##### Why can't I double-tap to self-cast or change wards with double-tap?

That is intended behaviour in my super compact layout, to prevent miscasts. <kbd>Alt</kbd>+<kbd>Key</kbd> should do self-cast or switch wards. Furthermore, double tap self cast is impossible if you are using quick casts.

This was done by disabling the `dota_ability_self_cast_timeout` tolerance. The way "double-taping" works is by using the "smart-double tap" in-game option (hold space and press an item or ability's hotkey).

##### Can I rebind stuff in-game?

You can change the bind of most things in-game but a few, you can only change by editing the `.cfg` files.

##### Why do some of my commands not trigger?

That must be because of your non-standard keyboard. You should consider changing your keyboard layout to standard English in Windows options.

##### Can I bind keys like <kbd>Shift</kbd>, <kbd>Escape</kbd>, <kbd>Ctrl</kbd>, Ping Key (Default: <kbd>Alt</kbd>), <kbd>Mouse 1</kbd>, <kbd>Mouse 2</kbd> and <kbd>Mouse 3</kbd>?

No. Those are specially coded keys in the source engine that sadly aren't supported for modification.


##### Does <kbd>CAPSLOCK</kbd> still do what it usually does, even if it's a keybind?

CapsLock will always be off in dota. You can change this in the OLite.ahk if you wish.

### How does it work?

The `autoexec.cfg` file is loaded and executed automatically by the dota2 client which acts as an engine which loads and combines other `.cfg` files into a flexible keyboard layout which is easy to modify.

Take a sniff through the files—there are plenty of explanatory comments in each `.cfg` file.

Each config file has its own role. Once you understand what they do, they're easy to tweak.

The `.ahk` script does not touch dota2.exe and will NOT get you banned. All the AHK script does is block Windows from seeing the Windows key presses sent to dota2.exe. It does not do anything that the SteamOS doesn't.


### Made a cool keyboard layout and want to share it?

Contact me and I might add it to the main repository for people to see, and I'll give you credit.
If you know how to use git, just fork this repo and request a merge using a pull request.
