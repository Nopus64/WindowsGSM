# WindowsGSM.Factorio
🧩Factorio Plugin for WindowsGSM

# Requirements
[WindowsGSM](https://github.com/WindowsGSM/WindowsGSM) >= 1.22.0

# Installation

1. Download the latest release
2. Move Factorio.cs folder to plugins folder
3. Click **RELOAD PLUGINS** button or restart WindowsGSM
    - Goto the **Plugin Area** on the bottom left at the WindosGSM. (_Puzzelsymbol_)
4. Click in **WindowsGSM Servers** then on **Install GameServer**
5. Click on the Dropdown Menu and Search for `Factorio Dedicated Server` [FACTORIO.cs]
    - Optional _Change Server Name_ (Can be done Later too)
6. Press Install (Enjoy ❤️)

# Additional Information

Not all is handled by Windows GSM due to Factorio Limitations (blame the devs):

1. Find the example file named "server-settings.example.json" under the directory:
`YOURDRIVELETTER\path\to\Steam\steamapps\common\Factorio\data\server-settings.example.json` (game installation directory)
2. Copy the file and put it under file path: C:\Users\Public\server-settings.example.json (for example)
    - It has to be a file path that has no strict permissions under, otherwise it will give you issues.
3. Rename the file to "server-settings.json"
4. Will try to automate this step but for now, you need to do it manually:
Open the file with an editor like [Visual Studio Code](https://code.visualstudio.com/Download) and input all the settings how you'll like.

"name": "MyServer",
"description": "MyDescription",

5. Input your LOGIN credentials for factorio.com in the section:

"_comment_credentials": "Your factorio.com login credentials. Required for games with visibility public",
"username": "MyUsername",
"password": "MyPassword",

**IMPORTANT!** You will need the login credentials whether or not you set the server to be PUBLIC or not. Else you'll get an ERROR for Connection failure with server.

**FINAL:**

With the examples above, the input of your "server.bat" file should look like this:

```
@echo off
start /wait Factorio.exe --start-server MySaveGame.zip --server-settings C:\Users\Public\server-settings.json
exit 0
```
