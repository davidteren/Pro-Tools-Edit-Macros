# Pro Tools - Automator Editing Macro

Pro Tools (De-Breath) Editing macro via Automator (Mac OS X)
Handy tool for dealing with those repetitive tasks.
This specific macro is handy for editing those nasty rushed radio commercials where the dialog is longer than the allocated flighting duration :)

### Usage ###

 - Copy the code below

```## Cut a breath (Ctrl + Alt + C)
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
end tell```

Create the Automator Preset
---------------------------
 - Open the Automator App!
 (https://github.com/davidteren/Pro-Tools-Edit-Macros/blob/master/images/01.png)
 - In the "Choose a type for your document" dialog pane select > Service & click the Choose button.
 - In the search field type"apple" and select "AppleScript" when it appears
 - Drag & drop the selected AppleScript icon into windo pane on the right
 - Select the existing code & replace it with the code we copied above these directions
 - Change the "Service receives" option to "no input"
 - Select "Other " in the next field & then select your Pro Tools app
 - Save the service CMD + S giving it an appropriate name
 - Close the Automator App
 
Create the Keyboard Shortcut
-------
 - In System Preferences got to Keyboard > Shortcuts
 - In the left pane select Services
 - In the right pane select your Automator service (probably at the bottom of the list)
 - Click the add shortcut button & press the key combination you want to use. Be sure not to use a key combo that will conflict with your version of Pro Tools
 -  - Check that the service is available and the Keyboard shortcut is assigned in Pro Tools in the Service menu. If not restart Pro Tools

Using the service
-------
 - Select the breath you want to delete & the area you want to shorten
 - Use your key combo to run the service (Hint: Press & release quickly)
 - You can use your combo twice or more time in succession to make longer gaps shorter.