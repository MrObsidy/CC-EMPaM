# CC-EMPaM
EMPaM - the ComputerCraft Extensible Modular Packet Manager.

# Installation:

I'm still setting up pastebin. Please be patient for a couple of days.

The program gets installed to /empam/. The main executable is /empam/empam, modules are loaded to /empam/modules/
and plugins can be installed to /empam/modules/plugins/.

# Usage:
empam --help for a list of commands. This explains everything.

# Writing plugins
To write a plugin, place a file (no extension!) into the /empam/modules/plugins/. The module pluginmgr will automatically
load all plugins in /empam/modules/plugins/.

All plugins must have the following global methods:
initialize() - this will be called when pluginmgr loads the plugin
getName() - this will be called whenever empam --plugin <name> and empam --plugins is called. The name that is returned here
  will be used for your plugin command.
printHelp() - Plugin information will be printed when empam --plugininfo is called.
execute(tArgs) - This is called whenever:
  - empam --plugin <yourpluginname> <args...> is called: <args..> is passed as a parameter
  - whenever a built-in command is called, args[] is passed
  
I will write a proper tutorial on how to write EMPaM plugins later.
