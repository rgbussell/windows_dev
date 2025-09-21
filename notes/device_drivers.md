Windows startup tasks can be modified with regedit
# Here is an example of stopping automating loads of steam audio device drivers at startup

Prevent Steam from Automatically Installing the DriversSteam loads these drivers by default for streaming. To skip this:Close Steam completely (check Task Manager to ensure no Steam processes are running).
Locate your Steam installation folder (usually C:\Program Files (x86)\Steam).
Right-click Steam.exe, select "Create shortcut," and place it on your desktop or elsewhere.
Right-click the new shortcut, select "Properties."
In the "Target" field, add a space after the existing path, then append -skipstreamingdrivers (e.g., "C:\Program Files (x86)\Steam\Steam.exe" -skipstreamingdrivers).
Click "OK" to save.
Use this shortcut to launch Steam from now on. This command line option tells Steam not to install or load the streaming drivers. 

If Steam is set to auto-start with Windows, you may also need to modify its startup entry:Press Windows + R, type regedit, and press Enter (approve the UAC prompt).
Navigate to HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run.
Find the "Steam" entry, right-click it, select "Modify," and add -skipstreamingdrivers to the end of the Value data field (similar to the shortcut).
Restart your PC and launch Steam to apply.

