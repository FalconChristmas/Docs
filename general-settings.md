# General Settings

### Blank screen on startup
Enable/Disable a screen blanker at FPP startup. If you are using a projector with your Pi to display video then you will want to enable this setting so that the text console does not show on your projector when you are not playing videos

### Force Analog Audio Output
Force audio output out the 1/8-inch stereo jack even when using HDMI for video

### Pi 2x16 LCD Enabled
Enable use of a LCD display attache to the Pi for status and control

### Always transmit channel data
Force transmission of channel data out to controllers whenever FPP is running. FPP will normally only transmit data when there is a sequence playing or the system is running in Bridge mode or a Pixel Overlay model is enabled. Some controllers go into test mode when not receiving data. This setting causes FPP to always send data so the controllers do not go into test mode.

### Audio Output Device
Allows controlling whether audio is sent out via the onboard soundcard or a USB attached soundcard or FM transmitter.

### Log Level
The E1.31 output can drive up to 128 universes (65,536 channels) over the Pi's ethernet network interface.

**Log Levels**

Level |	Description
------|------------
Warn |	Errors and warnings
Info |	Informational logs about state of the system.
Debug |	The Debug level generates verbose logs useful for debugging issues or configurations. This should not be enabled during normal use unless you are trying to track down an issue.
Excessive |	The Excessive level generates very detailed logs which are excessive enough to affect performance. Turning on Excessive level logging may cause parts of FPP to not function properly due to the excessive amount of logging. It is normally only used in specific cases with specific Log Masks configured.

### Log Mask 
The E1.31 output can drive up to 128 universes (65,536 channels) over the Pi's ethernet network interface.

**Log Masks**

Mask | Description
-----|------------
ALL | The ALL meta-value enables all debug logs at the selected level. This can be very verbose and is normally only recommended at the Warn or Info levels.
Most | The Most meta-value enables all debug logs except for Channel Data.
Channel Data | Log every time that channel data is sent out to controllers
Channel Outputs | Log info about the Channel Outputs themselves
Commands | Log received commands and their replies
Control Interface | Log info from the remote control interface
E1.31 Bridge | Log info about E1.31 bridge mode
Effects | Log info about Effects sequences
Events | Log info about Events triggered
General	 | General log info for miscellaneous areas of FPP
GPIO | Log GPIO Input events
Media Outputs | Log info about the media players that FPP uses.
MultiSync | Log info when syncing playback on multiple Pi's
Playlists | Log info when parsing playlists
Plugins | Plugin log info
Scheduler | Log info when scheduling playlists
Sequence Parser | Log info when playing sequences
Settings | Log info when parsing or applying settings
