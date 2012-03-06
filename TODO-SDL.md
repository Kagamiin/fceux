Features
========
	* SDL.Vsync
		* let's wait on this -- there's no simple way to use the OS default in SDL unless we just don't touch it, which might be the best thing to do here.
  
GTK
===
	* Better on-the-fly video resizing with window resize / video config
	* Hotkey remapping GUI
	* Smarter video config (disable widgets that are incompatible with openGL)
	* Options to investigate:
		* bpp
		* scanlines
	* Cheat editor

SDL 1.3
=======
	* segfaults when opening a second game
	* segfaults on fullscreen entry
	* haven't tested this in a while
	* not a 2.1.6 target

BUGS
====
	* Zipped rom support borked?
	* F1 from terminal-less gui fceux process hangs fceux (since input is required from console in cheat editor)

OSX
===
	* Single window mode does not work (the XWINDOWID hack does not work in Apple's X11 server, so this may never get fixed).
	* Zapper input is taken from GTK window instead of X11 window (a workaround could be implemented to resolve with with some #ifdef APPLE etc)
	* Not an "official" target, but testing should be done before release on OS X

DOCS
====
	* Be sure to include details about new scons features for package maintainers so that the manpage, luascripts, and auxlib will be included in future packages
	* Docs REALLY need a cleanup/rewrite