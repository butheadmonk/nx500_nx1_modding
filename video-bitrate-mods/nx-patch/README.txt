                  Samsung NX1 and NX500 nx-patch

                               v5.01
                               
     Copyright (C) 2016  Vasile Dumitrescu, (ppnx.vasile@dfgh.net)

     some components Copyright (C) 2016 Otto Kiksmaler
                                (https://github.com/ottokiksmaler)

   This program is free software; you can redistribute it and/or modify
   it under the terms of the GNU General Public License as published by
   the Free Software Foundation; either version 3 of the License, or
   (at your option) any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.

   You should have received a copy of the GNU General Public License
   along with this program; if not, write to the Free Software Foundation,
   Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301  USA

                          CHANGE LOG

Version 5.01 - 2016-06-12
  - now REQUIRES nx-on-wake mod, the new bluetooth-less launch architecture
  - no more delays in launch, mods are instantly available :-)
  - NX500 activation with EV EV
  - NX1 activation with OK OK (EV EV does not work on NX1)
  - nx-on-wake makes it possible to have this mod INSTANTLY available upon
    startup (bitrates are always permanently saved upon change)

Version 4.13 - 2016-06-03
  - 30 min video recording limit removed by default upon install
    and reinstated upon uninstall
  - replaced keyscan with new smaller version
  - no public release

Version 4.12 - 2016-05-30
  - while awaiting for the repaired burner cam to be able to work
    on hibernation image update
  - keyboard now shows (mostly) properly on NX1
  - mod user interface does NOT launch if in movie (record or play) mode
  - uninstall now requires positive confirmation
  - BUG: on NX1 if screen times out and goes in power saving it will take
    a a couple of more half-shutter to wake the screen up and dialogues will
    be dismissed as a result. [won't fix as too difficult for current version
    of the user interface - wait for a future version using another framework]
  - BUG: on NX1 upon uninstall the confirmation keyboard does not always appear
    just tap on the screen and it will [won't fix, same reason as above]

Version 4.11 - 2016-05-29
  - added uninstall

Version 4.1 - 2016-05-29
  - added automatic installer
  - this version uses keyscan, mod_gui, popup_*, tools
      (C) 2016 Otto Kiksmaler
  - bluetooth works
  - GUI shows current state of mods
  - mod state can be saved as default so as to be applied automatically
    upon bluetooth activation
  - user interface is activated by clicking EV key twice within 1 second
    (i.e. double click EV key)
  - BUG [NX1 only]: on the bit rate entry screen the keyboard does not always
    show up immediately. In this case just click somewhere on the screen in the
    zone where the keyboard should appear and it will. I am not sure what
    causes this but since I plan to replace this interface with a better
    one I do not want to spend a lot of time on this cosmetic issue.

Version 4.0 - 2016-05-27:
  - supports (only) NX500 v1.12 and NX1 v1.41
  - renamed to nx-patch as it is intended to contain more than just bitrate
    adjustments :-) (watch this space)
  - removed NX500 15 min UHD and 25 min FHD/50 and FHD/60 limits
  - enabled permanent DEV menu access without a "special" SD card file
      NB you still need to do the key dance to activate it
  - enabled (many) more video slots - see enclosed nx-patch.png
  - self-contained - does not rely on any additional scripts or on bash
		to identify camera model and version which should improve camera 
		stability through (much) lower memory requirements
  - improved safety and flexibility: only applies patches that are compatible
    with camera model on which it runs.
  - eliminated gdb :-) - program is now only 26kB
  - no longer needs a computer science degree to use it :-) uses 
    human-readable arguments :-)
  - behind the scene:
    + prepared for the future: I am now working on hibernation image
      integration (to dispose of BT and have instant-on patching) and since
      that WILL change memory addresses the patcher is now independent of
      memory address (i.e. it will support both original firmware and
      re-hibernated versions, as long as they report the same Samsung
      firmware version)
    + flexible architecture for instant integration of future patches

Version 3.0:
  - added 2.5k resolution

Version 2.0:
  - added support for more bit rate slots and for NX500

Initial version: v1.0
  - replaces NX1 80 Mbps video bit rate 

                              HOW TO

  0. The file containing this README.txt includes everything you need.
  1. Make sure the nx-on-wake mod is installed. This mod depends on nx-on-wake.
  2. The zip file includes a nx-patch.png file. Open and print it or
     familiarize yourself with it - it shows the meaning of the various
     bitrate and resolution slots. You will need to know them to use the mod.
  3. Unzip the file where you found this README in the root of your SD card.
  4. Insert the SD card into your camera and power it up. NB. I mean power 
     up the camera, not the SD card :-)
  5. Pay attention to the messages showing on the screen.
  6. You will be asked to power off and on the camera.
  7. Use EV EV (NX500) or EV AFON (NX1) to pop up the user interface.
  8. New bitrates are NOT remembered across cold boots. This is to reduce
     writes to the camera flash to the minimum necessary. Set them as defaults
     to change them permanently (across cold boots as well).

  A final word:
   If you find this program useful, I have a lens fund that only reached about
   half of its target :-) - your help would be much appreciated.

   goo.gl/7I67Rq      paypal: ppnx.vasile@dfgh.net
