# Using PPSSPP on iOS

This guide will show you how to use PPSSPP, the PSP emulator, on iOS.
It isn’t as simple as PPSSPP on Windows, but it is still possible, and
allows for great fun while away from the computer. This guide will
attempt to be as thorough and up-to-date as possible, so as things in
iOS emulation change, I’ll keep this guide as useful as possible.

## Things you’ll need

Since iOS emulation is a bit different from Windows, you’ll need to
make sure you have everything necessary to enjoy PSP games.

* An iPhone 7 or newer, or a recent iPad or iPod with an A10 CPU or
newer.
* A game controller: Xbox 1S, PS4, Game Vice Live, ETC. Any Made For
iPhone controller should work
* A Mac or Windows computer
* An Internet connection
* A few hours worth of Determination

## Getting Started with an alternative app store

Apple loves to control as much as possible on their platforms. This
doesn’t mean, however, that our journey ends here. There are
alternatives, but the one I’ll focus on in this article is AltStore.
It is a brilliant use of Apple’s own technology to install apps onto
your device. Where other stores face revocations of their developer
ID’s, AltStore uses an Apple ID’s own free developer access to sign an
app for seven days, renewing the signature every few days to make
things as close to permanent as anything in the Apple world is.

So, let’s get Altstore installed. In your web browser, go to
<https://altstore.io>. Here, download AltServer for your system, which
will handle the installation of AltStore onto your device, and install
it. Read the website for the steps to get things started. Install
AltStore, using AltServer, to your device. Now, go to settings,
General, Profiles, and trust the one with your Apple ID on it. Now,
you can open AltStore.

There are basically two tears to Altstore access. The free access
gives you Delta, which is an emulator for a few systems, including
SNES, N64, And Game Boy. The paid, Patreon-sponsored, beta version,
gives the ability to install one’s own apps, add different sources for
apps, and gives you a beta version of Delta, bringing Nintendo DS
support. Delta doesn’t currently have any accessibility features, but
I’ve [asked for
this](https://github.com/rileytestut/DeltaCore/issues/13). AltStore
also has a few problems, in the free and paid versions, and I’ve
[brought them up](https://github.com/rileytestut/AltStore/issues/145)
as well.

Accessibility issues aside, the service works, and hopefully accessibility
issues will be fixed. Until then, I’ll give you as much information as you need
to install apps, like PPSSPP.

## Installing PPSSPP

In earlier versions of the guide, I gave instructions on installing the AltStore
beta, adding a source, and installing PPSSPP from that source. This is no longer
necessary. Now, after installing AltStore, all you have to do is download an IPA,
which is an iOS app, and load it into AltStore for installation. The main reason
I‘m changing this is that the version of PPSSPP from all these sources is old
and out of date, and as many blind people know, the most up-to-date version of
programs can be either very good for accessibility, or very bad.

Luckily, the newest version of PPSSPP allows you to load games into it, just by
double tapping on them from the Files app. This drops the barrier to entry for
many blind people, who obviously don‘t like hunting in the dark, as it were, for
their games.

To download PPSSPP, open Safari on your iOS device and go to [this page](https://halo-michael.github.io/en_US/).
Here, click the link to download “PPSSPP”, under the “DOWNLOAD IPAS” text.

Now, open the Files app, navigate to your iCloud Drive‘s Downloads folder, and
find the IPA for PPSSPP. Double tap on it, and you‘ll be taken to AltStore.
Follow the instructions to install the app. Now, you should have PPSSPP on your
home screen.

## Configuring PPSSPP

Now, it’s time to do a little configuration. This will take the
longest, and be the most complicated part of the guide, so breathe in
some Stormlight, burn some Allomantic metal, or gather all the
investiture you have. On your iPhone, go into the Files app, then, in
the “On my iPhone” section, find the PPSSPP folder. Open that, in find
the PSP folder. Open that, and find the System folder. Open that, and
find the ppsspp.ini file. This is PPSSPP’s configuration file.

Drag the file, by flicking up to “drag”, then double tap. Now, go back
to the main files screen, and find an online file storage service you
like. You could use Google Drive, OneDrive, or iCloud Drive. Choose
that, and find a folder to drop the configuration file into. When you
are on the folder you want to drop the file into, not inside the
folder, swipe up to Drop, and double tap. Now, on your computer, find
that file, and open it with a text editor, like Notepad, or Text Edit.
Don’t open it with Microsoft Word, please.

In the PPSSPP configuration file, there are many sections. They are
like headings in a document. Headings consist of a word, or maybe a
phrase, enclosed in brackets, like:

	[General]

This means that at the top of the file is a section called “general.”

Configuration files allow you to configure a program by, basically,
giving information to prompts. Some information may be a number
standing for an item, and some may be text, like your name, while
others are binary options, true or false, meaning on or off.

For example, the line below the general section header is:

	FirstRun = False

This means that FirstRun is false. To expand upon that, it means hat
first run is off, meaning that this isn’t PPSSPP’s first run. This is
from my configuration file, though, so yours may say that it is the
first run, that first run is true.

Now, let’s actually do some configuration. I’ll show which things need
configuring, and expand on it afterwards.

	CPUCore = 2

This sets the CPU to 2, which, on iOS, is necessary to play games.
When iOS isn’t jailbroken, JIT, a quick interpreter, is not available.
So, we have to use a slower, and less optimized, CPU type: the IR Interpreter. However, on
my iPhone X R, and probably on even an iPhone 7, PPSSPP runs perfectly
for me.

	EnableWlan = True

If you want to play online, enable the wireless networking system.

	InternalScreenRotation = 0

This sets the screen rotation to “auto.” So, if you turn off lock
rotation, or don’t have it on, you can turn your device to
landscape without having to have in actually in reverse landscape
mode to play. This is useful for if sighted people want to play
your game, and you have a Game Vice Live controller, which
connects to your phone on either end, making it look like a mobile
game console, like a PSP.

	NickName = ppsspp

Set this to whatever you want your name to be. If you do this, your
name will automatically be filled in on PSP games which use that data.

	proAdhocServer = 

This line is to configure a place to connect to, for playing games
online with other people. If you want to play with just another
person, then put that person’s IP address in the place to the right of
the equals sign. Your configuration file may have something already to
the right of the equals sign. If you want to change it, you can
replace that part that is already there. Some servers, like “My
Neighbor Sushi Cat,” allow you to see how many people are playing on
which games, by visiting the address of the server in your browser.
You can find places to connect to at <https://ppsspp.org/adhoc.html>.

	MacAddress = 

The Mac address is a random address which differentiates your device
from others in a server or network, or something like that. This is,
at least, what it does in PPSSPP. If you play online, you’ll need to
make this different from the default. Perhaps you can use your phone’s
Mac Address to make it different enough.

Now, save that into iCloud Drive. If you already had it there, you
don’t have to move it there again. On your iPhone, drag and drop that
from iCloud Drive to On My iPhone, PPSSPP, PSP, System. Remember to
drop it on the System folder, not inside it. If you are asked if
you want to replace the file, replace it. Now, PPSSPP should be
configured. Well done; that was the hardest part of this guide. It’s
all easier from here.

## Loading games

Now that we have PPSSPP all configured, we can load some games! I
assume that you have your games on your computer. Put those in your
file storage system of choice; One Drive, iCloud Drive, Google Drive,
ETC. Now, on your iPhone, move those from the file storage place to
“On my iPhone”, PPSSPP. You can load them from other local storage spaces, but iCloud Drive doesn‘t seem to work for loading games.

Now, turn off lock rotation if you’d like, and connect your
controller. After that’s done, open PPSSPP. You‘ll probably need to do this so that you can register it with the share sheet. Now, go to the Files app, find the game, and double tap on it. If it doesn‘t automatically open in PPSSPP, share it with that app. Now, the game loads, and you can have fun!

## Special notes for controllers

On Made For iPhone controllers, the start button is R2, and select is
L2. The Menu, or Start, button opens the PPSSPP menu, which is not accessible.

# Games known to not work on PPSSPP for iOS

* Soul Calibur: Broken Destiny

