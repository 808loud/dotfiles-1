# \\[._.]/ - Hi, I'm the OSX bot

I will update your OSX machine with better system defaults, preferences, software configuration and even auto-install some handy development tools and apps that my developer friends find helpful.

You don't need to install or configure anything upfront! This works with a brand-new machine from the factory as well as an existing machine that you've been working with for years.

# Forget About Manual Configuration!

Don't you hate getting a new laptop or joining a new team and then spending a whole day setting up your system preferences and tools? Me too. That's why we automate; we did it once and we don't want to do have to do it again.

\\[^_^]/ - This started as Adam Eivy's OSX shell configuration dotfiles but has grown to a mutil-developer platform for machine configuration.

When I finish with your machine, you will be able to look at your command-line in full-screen mode like this (running iTerm):

![iTerm Screenshot](https://raw.githubusercontent.com/atomantic/dotfiles/master/img/dotfiles.png)

Check out how your shell prompt includes the full path & the working git branch!
\\[._.]/ - I'm so excited I just binaried in my pants!

# Watch me run!
![Running](http://media.giphy.com/media/5xtDarwenxEoFeIMEM0/giphy.gif)

# Running

Note: I recommend forking this repo in case you don't like anything I do and want to set your own preferences (and pull request them!)
```bash
git clone --recurse-submodules https://github.com/808loud/dotfiles-1 ~/.dotfiles
cd ~/.dotfiles;
./install.sh;
```

> Note: running install.sh is idempotent. You can run it again and again as you add new features or software to the scripts! I'll regularly add new configurations so keep an eye on this repo as it grows and optimizes.

# Restoring Dotfiles

If you have existing dotfiles for configuring git, zsh, vim, etc, these will be backed-up into ~/.dotfiles_backup and replaced with the files from this project. You can restore your original dotfiles by using `./restore.sh`

# ¯\\_(ツ)_/¯ Warning / Liability
> Warning:
The creator of this repo is not responsible if your machine ends up in a state you are not happy with. If you are concerned, look at install.sh and osx.sh to review everything this script will do to your machine :)

# Additional

There are a few additional features in this repo:

- .crontab: you can `cron ~/.crontab` if you want to add my nightly cron software updates.

> \\[0_0]/ - Note that this may wake you in the morning to compatibility issues so use only if you like being on the edge

# Settings
This project changes a number of settings and configures software on OSX.
Here is the current list:

## Configuring General System UI/UX
- Disable local Time Machine snapshots
- Disable hibernation (speeds up entering sleep mode)
- Remove the sleep image file to save disk space
- Set a custom wallpaper image

## Standard System Changes
- always boot in verbose mode (not OSX GUI mode)
- allow 'locate' command
- Set standby delay to 24 hours (default is 1 hour)
- Disable the sound effects on boot
- Menu bar: disable transparency
- Menu bar: hide the Time Machine, Volume, User, and Bluetooth icons
- Set highlight color to green
- Set sidebar icon size to medium
- Always show scrollbars
- Increase window resize speed for Cocoa applications
- Expand save panel by default
- Expand print panel by default
- Save to disk (not to iCloud) by default
- Automatically quit printer app once the print jobs complete
- Disable the “Are you sure you want to open this application?” dialog
- Remove duplicates in the “Open With” menu (also see 'lscleanup' alias)
- Display ASCII control characters using caret notation in standard text views
- Disable automatic termination of inactive apps
- Disable the crash reporter
- Set Help Viewer windows to non-floating mode
- Reveal IP, hostname, OS, etc. when clicking clock in login window
- Restart automatically if the computer freezes
- Never go into computer sleep mode
- Check for software updates daily, not just once per week
- Disable Notification Center and remove the menu bar icon
- Disable smart quotes as they’re annoying when typing code
- Disable smart dashes as they’re annoying when typing code

## Trackpad, mouse, keyboard, Bluetooth accessories, and input
- Trackpad: enable tap to click for this user and for the login screen
- Trackpad: map bottom right corner to right-click
- Disable “natural” (Lion-style) scrolling
- Increase sound quality for Bluetooth headphones/headsets
- Enable full keyboard access for all controls (e.g. enable Tab in modal dialogs)
- Use scroll gesture with the Ctrl (^) modifier key to zoom
- Follow the keyboard focus while zoomed in
- Disable press-and-hold for keys in favor of key repeat
- Set a blazingly fast keyboard repeat rate:
- Set language and text formats (english/US)
- Disable auto-correct

## Configuring the Screen
- Require password immediately after sleep or screen saver begins
- Save screenshots to the desktop
- Save screenshots in PNG format (other options: BMP, GIF, JPG, PDF, TIFF)
- Disable shadow in screenshots
- Enable subpixel font rendering on non-Apple LCDs
- Enable HiDPI display modes (requires restart)

## Finder Configs
- Allow quitting via ⌘ + Q; doing so will also hide desktop icons
- Disable window animations and Get Info animations
- Set Desktop as the default location for new Finder windows
- Show hidden files by default
- Show all filename extensions
- Show status bar
- Show path bar
- Allow text selection in Quick Look
- Display full POSIX path as Finder window title
- When performing a search, search the current folder by default
- Disable the warning when changing a file extension
- Enable spring loading for directories
- Remove the spring loading delay for directories
- Avoid creating .DS_Store files on network volumes
- Disable disk image verification
- Automatically open a new Finder window when a volume is mounted
- Use list view in all Finder windows by default
- Disable the warning before emptying the Trash
- Empty Trash securely by default
- Enable AirDrop over Ethernet and on unsupported Macs running Lion
- Show the ~/Library folder
- Expand the following File Info panes: “General”, “Open with”, and “Sharing & Permissions”

## Dock & Dashboard
- Enable highlight hover effect for the grid view of a stack (Dock)
- Set the icon size of Dock items to 36 pixels
- Change minimize/maximize window effect to scale
- Minimize windows into their application’s icon
- Enable spring loading for all Dock items
- Show indicator lights for open applications in the Dock
- Don’t animate opening applications from the Dock
- Speed up Mission Control animations
- Don’t group windows by application in Mission Control
- Disable Dashboard
- Don’t show Dashboard as a Space
- Don’t automatically rearrange Spaces based on most recent use
- Remove the auto-hiding Dock delay
- Remove the animation when hiding/showing the Dock
- Automatically hide and show the Dock
- Make Dock icons of hidden applications translucent
- Make Dock more transparent
- Reset Launchpad, but keep the desktop wallpaper intact
- Add iOS Simulator to Launchpad

## Configuring Hot Corners
- Top left screen corner → Mission Control
- Top right screen corner → Desktop
- Bottom right screen corner → Start screen saver

## Configuring Safari & WebKit
- Set Safari’s home page to ‘about:blank’ for faster loading
- Prevent Safari from opening ‘safe’ files automatically after downloading
- Allow hitting the Backspace key to go to the previous page in history
- Hide Safari’s bookmarks bar by default
- Hide Safari’s sidebar in Top Sites
- Disable Safari’s thumbnail cache for History and Top Sites
- Enable Safari’s debug menu
- Make Safari’s search banners default to Contains instead of Starts With
- Remove useless icons from Safari’s bookmarks bar
- Enable the Develop menu and the Web Inspector in Safari
- Add a context menu item for showing the Web Inspector in web views

## Configuring Mail
- Disable send and reply animations in Mail.app
- Copy email addresses as 'foo@example.com' instead of 'Foo Bar <foo@example.com>' in Mail.app
- Add the keyboard shortcut ⌘ + Enter to send an email in Mail.app
- Display emails in threaded mode, sorted by date (oldest at the top)
- Disable inline attachments (just show the icons)
- Disable automatic spell checking

## Spotlight
- Disable Spotlight indexing for any volume that gets mounted and has not yet been indexed
- Change indexing order and disable some file types from being indexed
- Load new settings before rebuilding the index
- Make sure indexing is enabled for the main volume

## iTerm2
- Installing the Solarized Dark theme for iTerm
- Don’t display the annoying prompt when quitting iTerm
- hide tab title bars
- set system-wide hotkey to show/hide iterm with ^`

## Time Machine
- Prevent Time Machine from prompting to use new hard drives as backup volume
- Disable local Time Machine backups

## Activity Monitor
- Show the main window when launching Activity Monitor
- Visualize CPU usage in the Activity Monitor Dock icon
- Show all processes in Activity Monitor
- Sort Activity Monitor results by CPU usage

## Address Book, Dashboard, iCal, TextEdit, and Disk Utility
- Enable the debug menu in Address Book
- Enable Dashboard dev mode (allows keeping widgets on the desktop)
- Use plain text mode for new TextEdit documents
- Open and save files as UTF-8 in TextEdit
- Enable the debug menu in Disk Utility

## Mac App Store
- Enable the WebKit Developer Tools in the Mac App Store
- Enable Debug Menu in the Mac App Store

## Messages
- Disable automatic emoji substitution (i.e. use plain text smileys)
- Disable smart quotes as it’s annoying for messages that contain code
- Disable continuous spell checking

## Google Chrome & Google Chrome Canary
- Allow installing user scripts via GitHub Gist or Userscripts.org

## SizeUp.app
- Start SizeUp at login
- Don’t show the preferences window on next start

## Atom Editor Text
- Install [Atom](https://atom.io/)

# Contributions
Contributions are always welcome in the form of pull requests with explanatory comments.

Please refer to the [Contributor Covenant](https://github.com/atomantic/dotfiles/blob/master/CODE_OF_CONDUCT.md)

# Loathing, Mehs and Praise
1. Loathing should be directed into pull requests that make it better. woot.
2. Bugs with the setup should be put as GitHub issues.
3. Mehs should be > /dev/null
4. Praise should be directed to [@antic](http://twitter.com/antic) or [@matthewmccull](http://twitter.com/matthewmccull) or [@mathiasbynens](https://github.com/mathiasbynens/dotfiles)


# Release History

### <sup>v1.1.0</sup>
 * Added dotfiles backup and restore.sh script
     * you can now restore your previous dotfiles with ./restore.sh
 * prompting the user more (e.g. `brew upgrade` is now optional)
