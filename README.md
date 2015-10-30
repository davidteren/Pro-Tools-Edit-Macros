# Pro Tools - Automator Editing Macro

Pro Tools (De-Breath) Editing macro via Automator (Mac OS X)
Handy tool for dealing with those repetitive tasks.

### Usage ###

* Download, unzip & double-click "PT-Cut Breath.workflow" to install
* In Apple Automator you can tweak to taste.


`## Cut a breath (Ctrl + Alt + C)
tell application "Pro Tools First"
  activate
  tell application "System Events" to key code 120 -- F2 -> Slip Mode
  delay 0.09
  tell application "System Events" to keystroke (ASCII character 127) -- Delete
  delay 0.02
  tell application "System Events" to keystroke (ASCII character 9) using {shift down} -- Shift + Tab 
  delay 0.02
  tell application "System Events" to keystroke "L" using {shift down, control down, option down, command down} -- Shift + Cntrl + Opt + Cmnd + L
  delay 0.02
  tell application "System Events" to key code 122 -- F1 -> Shuffle Mode
  delay 0.02
  tell application "System Events" to keystroke (ASCII character 127) -- Delete
  delay 0.02
  tell application "System Events" to key code 120 -- F2 -> Slip Mode
end tell`