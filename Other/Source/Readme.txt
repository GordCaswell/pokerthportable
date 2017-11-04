PokerTH Portable Launcher 1.4
=============================
Copyright 2004-2007 John T. Haller

Website: http://PortableApps.com/PokerTHPortable

This software is OSI Certified Open Source Software.
OSI Certified is a certification mark of the Open Source Initiative.

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

ABOUT PokerTH PORTABLE
======================
The PokerTH Portable Launcher allows you to run PokerTH from a removable drive whose letter changes as you move it to another computer.  The game and your settings are be entirely self-contained on the drive and then used on any Windows computer.


LICENSE
=======
This code is released under the GPL.  Within the PokerTHPortableSource directory you will find the code (PokerTHPortable.nsi) as well as the full GPL license (License.txt).  If you use the launcher or code in your own product, please give proper and prominent attribution.


INSTALLATION / DIRECTORY STRUCTURE
==================================
By default, the program expects one of these directory structures:

-\ <--- Directory with PokerTHPortable.exe
	+\App\
		+\PokerTH\
	+\Data\
		+\settings\

OR

-\ <--- Directory with PokerTHPortable.exe
	+\PokerTHPortable\
		+\App\
			+\PokerTH\
		+\Data\
			+\settings\

It can be used in other directory configurations by including the PokerTHPortable.ini file in the same directory as PokerTHPortable.exe and configuring it as details in the INI file section below.  The INI file may also be placed in a subdirectory of the directory containing PokerTHPortable.exe called PokerTHPortable or 2 directories deep in PortableApps\PokerTHPortable or Data\PokerTHPortable.  All paths in the INI should remain relative to the EXE and not the INI.


PokerTHPORTABLE.INI CONFIGURATION
================================
The PokerTH Portable Launcher will look for an ini file called PokerTHPortable.ini within its directory.  If you are happy with the default options, it is not necessary, though.  There is an example INI included with this package to get you started.  The INI file is formatted as follows:

[PokerTHPortable]
PokerTHDirectory=App\PokerTH
SettingsDirectory=Data\settings
PokerTHExecutable=PokerTH.exe
AdditionalParameters=
DisableSplashScreen=false

The PokerTHDirectory and SettingsDirectory entries should be set to the *relative* path to the directories containing PokerTH.exe and your settings from the current directory.  All must be a subdirectory (or multiple subdirectories) of the directory containing PokerTHPortable.exe.  The default entries for these are described in the installation section above.

The PokerTHExecutable entry allows you to set the PokerTH Portable Launcher to use an alternate EXE call to launch firefox.  This is helpful if you are using a machine that is set to deny PokerTH.exe from running.  You'll need to rename the PokerTH.exe file and then enter the name you gave it on the PokerTHexecutable= line of the INI.

The AdditionalParameters entry allows you to pass additional commandline parameter entries to PokerTH.exe.  Whatever you enter here will be appended to the call to firefox.exe.

The DisableSplashScreen entry allows you to run the PokerTH Portable Launcher without the splash screen showing up.  The default is false.
