IT HELP DESK WORD INSERTER - VERSION 1.06
Created by Luiz Holt
BAT / PowerShell edition - no registration required

A Windows snippet manager for incident tickets, troubleshooting work notes,
user communications, escalation handoffs, and resolutions.

START
1. Extract the entire ZIP to a permanent folder on your Windows computer.
2. Keep all six program files together. Double-click Start-Snippet-Manager.bat.
3. The command window minimizes while the program opens. Leave that minimized
   window running. Exit through File > Exit or the system tray > Exit.
4. On first use, a desktop shortcut named IT Help Desk Word Inserter is created
   with the custom icon. It points to the extracted folder; keep the folder in
   the same location so the shortcut continues working.
5. Start-Snippet-Manager.vbs is an optional minimized launcher if VBScript is
   enabled on your computer. The BAT launcher is the primary method.

Requires Windows PowerShell 5.1 and the built-in .NET Framework. No account,
registration, paid software, internet connection, or administrator access is
required. Organization-managed computers may block PowerShell or shortcuts;
follow your organization's approved software process if this occurs.
The tray icon may be under Windows' hidden-icons arrow near the clock.

WHAT IS INCLUDED
- 25 editable IT help desk samples in five categories: Intake, Troubleshooting,
  User Updates, Escalation, and Resolution. No travel or email sample set.
- Searchable snippet titles, categories, text, and auto triggers.
- Dark mode, configurable floating reference, and saved preferences.
- First-use desktop shortcut plus custom desktop, program, and tray icon.
- Import/Export backups, duplicate-trigger checking, and a quick pause toggle.
- Help > Read Me opens this file. Help > About displays program information
  and the credit Created by Luiz Holt.

HOW "INSERT INTO APP" WORKS
The button pastes the selected snippet where your cursor was in another app.
Open the manager with its keyboard shortcut so it knows the destination:
1. Open your ticketing system, Notepad, email editor, or other destination app.
2. Click the field where you want the snippet inserted.
3. Press Ctrl + Alt + Space, then release the keys. The manager opens.
4. Select a snippet and click Insert into app. Double-clicking the snippet or
   pressing Enter while the search box or list is focused also works.
5. The manager hides, returns to your original app, and pastes the text.
   Briefly wait while it inserts; do not click or type during insertion.

If you open the manager normally (such as through the desktop shortcut or
tray icon), it may not know your destination. In that case, Insert into app
copies the selected snippet instead. Click your destination field and press
Ctrl + V to paste. The status message tells you when this happens.

MANUAL COPY AND PASTE
Select a snippet and click Copy text. Then click the destination field and
press Ctrl + V. This option is useful whenever automatic insertion is blocked
by the destination's focus rules or permissions.

Try the insertion sequence in Notepad first before using your ticket system.
If text is selected in the destination, pasting will replace that selection.

AUTO TRIGGERS
Each snippet can have an optional unique trigger, for example ;intake.
1. Keep the program running and make sure the indicator reads Autotext: ON.
2. Click your destination field, type ;intake, then press and release Space.
3. The trigger and space are replaced with the snippet plus a trailing space.

Triggers are case-insensitive and unique across categories. Use up to 40 ASCII
letters, numbers, or punctuation characters with no spaces. A leading semicolon
helps prevent accidental expansion. Type a trigger at the start of a field or
after whitespace without pausing for more than 5 seconds. Space activates the
expansion; Enter and Tab do not. Release Space and briefly wait. Very fast
continued typing can cancel insertion. The program stops insertion if you type,
click, or change the destination while it is inserting. Triggers do not expand
inside the program's own windows.

Pause using the main Pause autotext checkbox, Tools > Pause autotext, the
floating Options menu, or the tray menu. The main and floating windows show
Autotext: ON, PAUSED, or unavailable. Pausing triggers does not disable manual
Copy text or the shortcut picker. Duplicate triggers are rejected on save and
when importing a backup.

FLOATING REFERENCE WINDOW
The separate floating window lists only snippet titles and auto triggers;
it does not show snippet bodies. It is a reference to help you remember triggers.
- View > Show floating window shows or hides it. Closing its X hides it while
  the main program continues running.
- Choose Snippets, View > Choose floating snippets, or floating Options >
  Include / exclude snippets opens the checklist. Check the snippets you want,
  uncheck those you do not want, then Save. Select all and Select none are available.
- Hiding a snippet from this list does NOT disable its trigger or remove it
  from the main manager. New snippets appear in the reference by default.
- Add New Snippet opens the main program and its blank new-snippet form,
  ready for a title, category, optional trigger, and text.
- Options > Open main program opens the manager without starting a new snippet.
- Always on top can be toggled in the main View menu or floating Options menu.
- Drag the title bar to move the window; drag its edges to resize it.

DARK MODE AND SAVED PREFERENCES
View > Dark mode toggles light/dark colors. Dark mode is the initial default.
The program remembers the theme, window positions and sizes, floating visibility,
which snippets are included, always-on-top choice, and autotext pause state.
Window positions are brought back onto an available monitor when restored.
Preferences apply to this Windows user and this IT edition.

EDITING AND USING TICKET SAMPLES
New snippet creates a snippet; Edit changes the selected snippet; Delete removes
it after confirmation. Categories lets you add, rename, or delete categories.
Deleting a category moves its snippets into another category.

Bracketed text such as [User Name], [Device Name], [Ticket Number], and
[Troubleshooting Performed] is a placeholder. Replace it manually with the real
information after insertion, then review the ticket before saving or sending it.
Placeholders are plain text; this version does not prompt for values.
Samples are templates, not claims that troubleshooting or resolution has occurred.
Record only actions actually performed and facts verified. Follow your service
desk's priority, security, identity verification, and closure procedures.
Do not include passwords, authentication codes, or unnecessary sensitive data.

DATA AND BACKUPS
IT edition data is stored separately from the original snippet tool at:
%LOCALAPPDATA%\ITHelpDeskWordInserter\snippets.json
Preferences are in preferences.json in that same directory.
The original tool's saved snippets are not loaded or overwritten by this edition.
Close the original tool before running this one so the global shortcut is free.

Snippet edits save after Save. A .bak file preserves the previous saved version.
Use File > Export backup (or Export) for a JSON backup of categories and snippets.
Use File > Import backup (or Import), select your JSON file, then choose:
- Merge (recommended/default): keep the current collection and add imported
  snippets. Exact duplicates (same title, category, text, and trigger) are skipped.
  Existing triggers remain unchanged. If an imported trigger is already in use,
  the imported snippet is still added, but its trigger is left blank. A summary
  lists the conflicts; click Edit on those snippets to assign new triggers.
- Replace: use only the imported collection. A second confirmation warns that
  your current items will be removed. Cancel leaves the collection unchanged.

Category names are matched without regard to capitalization. Different snippets
with the same title are kept. Imported entries get distinct IDs if needed so
floating-list preferences do not get applied to unrelated snippets. The previous
saved collection is retained in snippets.json.bak when the import saves.

If an earlier Replace import removed the built-in samples, choose File > Add
IT ticket samples. This merges the 25 samples back into your current collection
without removing your own items. Exact duplicates are skipped. You can then
Merge your exported custom items into the same collection.

Backups contain snippets and triggers; interface
preferences and floating inclusion choices are stored separately on this computer.

If saved snippet data becomes unreadable, the program preserves it and opens
read-only. Close the program before restoring snippets.json.bak. Rename the
unreadable file first, then copy the .bak file to snippets.json and restart.
Keep exported backups in a location you control. Data and backups are not encrypted.

DESKTOP SHORTCUT
The first successful launch creates the shortcut once. Deleting it later does
not force the app to recreate it at every launch. You can create a shortcut to
Start-Snippet-Manager.bat yourself, or delete desktop-shortcut-created.txt from
this edition's data folder and restart to request first-use creation again.
If you move the extracted folder, update the shortcut target, working folder,
and icon, or remove that marker and relaunch from the new folder.

EXIT AND TROUBLESHOOTING
Escape or the main window's X hides the manager; it remains running in the tray.
Use File > Exit or tray > Exit to quit the app, floating window, and background
PowerShell process. Closing the minimized command window also stops the app.

Automatic insertion uses the clipboard and a paced Ctrl + V shortcut. It
replaces the clipboard contents and does not restore or clear them afterward.
Clipboard history or synchronization may retain copied text.
Password fields, some remote desktop environments, or administrator-level
programs may block automatic insertion. Use manual Copy text and paste instead.
The tool cannot bypass an application's restrictions.

If another app owns Ctrl + Alt + Space, the tool reports that the shortcut is
unavailable. Use the tray icon and manual Copy text. If Windows blocks autotext
hooks, the status indicator reports unavailable; Copy text remains usable.
The keyboard hook checks for triggers while running. It keeps only a short
in-memory buffer, never saves your typing to disk, and sends nothing online.
Non-ASCII triggers and Windows IME composition are unsupported; use the picker.
Plain text only: no images, rich-text formatting, macros, or cloud sharing.

VALIDATION
C# compilation, sample data, backup roundtrips, duplicate-trigger rejection,
preference saving/reloading, theme controls, floating-list inclusion, and the
blank new-snippet form were checked. Interface checks used a Linux compatibility
runtime with Windows hotkeys and hooks excluded. The Windows-only GUI,
PowerShell launcher, first-use shortcut, system tray, keyboard hooks, and actual
paste behavior require a Windows computer for end-to-end testing. Start with
Notepad, then test in your approved ticketing application.
