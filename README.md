# PluginPie

This library allows for the creation of plugins to extend your application.
Plugins are loaded dynamically at runtime.

# Usage

The following things are required by plugins:
- A main file
- In your mail file, a main plugin class with a name should be suffixed with `Plugin` (case sensitive) should exist.
- In your main plugin class, the following class attributes are required:
	- `ID`: an unique UUID4 string, this is what others will use to interact with your plugin
	- `NAME`: name of your plugin
	- `AUTHOR`: Name of author
	- `DESCRPTION`: A short description of your plugin
	- `VERSION`: a tuple of 3 ints
	- `WEBSITE`: This one is optional. Maybe your website, email or anyway to contact you.
- A free function called `init`, which takes no arguments should return your main plugin class **(Note: not an instance of your main class)**.

Putting all of this together we get the following:

My file:
```
- mainfileplugin.py
```

In `mainfileplugin.py`:
```
class MyPluginPlugin:
	ID = "00000000-0000-0000-0000-000000000000"
	NAME = "MyPlugin"
	AUTHOR = "Pewpews"
	DESCRIPTION = "MyPlugin makes you a happy panda!"
	VERSION = (1, 0, 0)
	WEBSITE = "https://github.com/Pewpews/happypanda"

def init():
	return MyPluginPlugin
```

# TODO

- Explain how to create hooks
- Finish this project...

