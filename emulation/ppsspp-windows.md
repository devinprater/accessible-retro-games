# Using PPSSPP on Windows

PPSSPP is easy to get set up with on Windows, but can take some time
to configure. It runs very well on laptops, just try to have at least
four gigabytes of RAM onboard. If you need help, just let me know.

## Downloading

To download the emulator, go to [PPSSPP's home
page](https://ppsspp.org), find the downloads link, then find the
"PPSSPP for Windows" heading. Once there, I recommend using the
installer, shown like "windows-36-white.png Download 1.9.3 Installer",
as it places the PPSSPP configuration files, save files, game data,
and other such user-facing material, in your documents folder. This
should be sent to OneDrive, if you’ve enabled that, allowing easy play
across all of your Windows devices. This also makes it easy to
transfer saves to iOS, if you want to play while not on the PC.

For this guide, I’ll pretend you went with the installer. If you get
the boring zip file, you should extract it, and everything will be in
folders in the zip file. You could also install PPSSPP through the
[Chocolatey package manager](https://chocolatey.org), and it should
put things like the installer.

## Configuration

Once PPSSPP is installed, you can configure it. Find the PPSSPP folder
in your Documents folder. In there, open the PSP folder, and find the
system folder. In the system folder, you’ll find "ppsspp.ini". If the
configuration files aren’t there, you may have to run PPSSPP first.
Find it in the Start menu, run it, then close it, to be sure that the
configuration file is created.

In the PPSSPP configuration file, there are many sections. They are
like headings in a document. Headings consist of a word, or maybe a
phrase, enclosed in brackets, like:

	[General]

This means that at the top of the file is a section called "general."

Configuration files allow you to configure a program by, basically,
giving information to prompts. Some of the information may be a number
standing for an item, and some may be text, like your name, while
others are binary options, true or false, meaning on or off.

For example, the line below the general section header is:

	FirstRun = False

This means that FirstRun is false. To expand upon that, it means  that
first run is off, meaning that this isn’t PPSSPP’s first run. This is
from my configuration file, though, so yours may say that it is the
first run, that first run is true.

Now, let’s actually do some configuration. I’ll show which things need
configuring, and expand on it afterwards.

	EnableWlan = True

If you want to play online, enable the wireless networking system.

	NickName = ppsspp

Set this to whatever you want your name to be. If you do this, your
name will automatically be filled in on PSP games which use that data.

	proAdhocServer = 

This line is to configure a place to connect to, for playing games
online with other people. If you want to play with just another
person, then put that person’s IP address in the place to the right of
the equals sign. Your configuration file may have something already to
the right of the equals sign. If you want to change it, you can
replace that part that is already there. Some servers, like "My
Neighbor Sushi Cat," allow you to see how many people are playing on
which games, by visiting the address of the server in your browser.
You can find places to connect to at <https://ppsspp.org/adhoc.html>.

	MacAddress = 

The Mac (Media Access Control) address is a random alphanumeric sequence that is tied to your NIC (Network Interface Card) and uniquely identifies your device on a network. If you play online, you’ll need to
make this different from the default. Perhaps you can use your
computer’s Mac Address to make it different enough.

## Playing a game

Now that you’ve gotten PPSSPP configured, you can load a game to play.
To load a game, press **Control + O**. This will open the "Open"
dialog box, where you can choose your game. I recommend creating a
"games" folder somewhere, like your OneDrive folder, where they can
all be synchronized across all of your devices. Once you’ve found a
game, press **Enter**, and it’ll then start. You can then use the OCR
capabilities of NVDA or JAWS, or just use sound and memorization, to
play the game.
