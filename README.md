# OpenXTalk-NSColorLists
An OpenXTalk Extension that wraps Apple's NSColor Swatches API

This xBuilder module binds to Apple's NSColorList methods to retrieve lists of
colors normally found in sections of the System's Color Picker dialogs,
including user defined color swatch lists.

The color list named "System" contains the current macOS UI theme colors, which may
be changed at any time by user's in the system settings. These are special dynamic colors,
meant to be used by app interface developers.

The highlight colors or the text selection color may be changed by the user.
Additionally the users dark/light appearance setting and accessibility settings
can effect some of these special colors. So it's important to re-check any of the
named swatches values that you may be using for any non-native parts/controls/widgets,
and update them accordingly in your scripts. In contrast, native cocoa controls
such as a 'default button', should change colors automatically. A good places in
your script to check for system color changes are handling the resumeStack message
and/or a systemAppearenceChanged (currently a macOS-only engine message) handler.
