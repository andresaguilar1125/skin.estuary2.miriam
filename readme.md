# Skin Estuary Mod V2
It's strongly recommended to install the skin via the "Kodinerds Repo", as this is the only way to guarantee that additional required modules (e.g. the PVR Artwork Module) are also installed. Another advantage is that you get automatic updates when 
you install an addon from a repository and not from ZIP.

## Repository URL
To install the Kodinerds repository visit the page "https://repo.kodinerds.net", download the repository zip (red button) and install it. After that you can install the skin directly from the repository under "Look & Feel", "Skins". Or just install the addons and dependecies for the skin. Dependencies can be installed without its python libraries




# XML Skin

## Settings.xml
- Added exit button to replace power dialog and keep a single screen

## Home.xml
- Onload activate tvchannels screen

## MyPVRChannels.xml
- Disable onleft + onright to avoid selecting scrollbar
- If not playingtv and channel is working then playpvrtv
- Force view53 for big list

## IncludesPVR.xml
- Modified BigList to increase font size
- Modified PVRInfoPanel to add text for channel guide
- Added font for channel input

## Font.xml
- Added custom size font for channel input
- Added custom size font for time on tvchannels

## DialogPVRChannelsOSD.xml
- Close dialogs

## DialogContextMenu.xml
- Conditional close dialog to avoid context menu instead of selecting channels

## DialogConfirm.xml
- Added conditional visibility, autoclose and playpvrtv on tvchannels and startup screens

## Startup.xml
- Replaced splash and logo screen

## Custom_1109_TopBarOverlay.xml
- Removed Time from top bar on OSD

## Custom_1135_PVROverlay.xml
- Added custom osd info on OSD when changing channels

## DialogSeekBar.xml
- Removed all controls and left channel number input only

## Includes.xml
- Comment on system time to remove if necessary

## VideoOSD.xml
- Remove all controls
- Added close to avoid enter on the remote control

## Custom_1143_VideoInfo.xml
- Remove info osd 




# Changes Kenwood TV

## Disable apps
To disable on kenwood tv apps on TV Quick Actions Pro enable ADB able to run some apps and create following adb commands

Disable apps on startup or wakeup screen
- pm disable-user --user 0 com.disney.disneyplus
- pm disable-user --user 0 com.apple.atve.androidtv.appletv
- pm disable-user --user 0 com.wbd.stream
- pm disable-user --user 0 com.amazon.amazonvideo.livingroom
- pm disable-user --user 0 com.netflix.ninja
- pm disable-user --user 0 com.google.android.youtube.tvmusic

Force stop kodi on power button keystroke
- am force-stop org.xbmc.kodi
- adb shell reboot --poweroff

## Keymaps 
Use keymap-editor addon on kodi if keymaps.xml file not working properly (Edit > Global > Windows > Open Shutdown Menu > Select Button). Must be disabled on TV Quick Actions Pro. Use the Keycode ID
- 61667 red
- 61668 green
- 61669 yellow
- 61670 blue

Remap the following keys
- Fullscreenlivetv : Back key > Live TV