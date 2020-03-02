# Inspiration
- https://github.com/mathiasbynens/dotfiles
- https://github.com/driesvints/dotfiles
- https://driesvints.com/blog/getting-started-with-dotfiles/

## Fresh install flow for macOS

### Prepare the machine
1. Update macOS to the latest version with the App Store
2. Install Xcode from the App Store, open it and accept the license agreement
3. Install macOS Command Line Tools by running `xcode-select --install`
4. Install homebrew (https://brew.sh/)

### Transfer SSH keys
Copy your public and private SSH keys to `~/.ssh` and make sure they're set to `600`

### Pull down the dotfiles repo
```
git clone https://github.com/tylerxo/dotfiles.git ~./dotfiles && cd ~/.dotfiles
```

### Run `brew.sh` to install packages and applications
```
source brew.sh
```

### Create symlinks to files
```
source link.sh
```

### Set MacOS Preferences
```
./.macos
```

After running all of these steps, restart the computer.

## Maintaining Dotfiles
- When installing a new app, tool or font, try to install it with Homebrew and add it to your Brewfile
- When configuring a new app make sure to run mackup backup to save your preferences
- When changing an macOS setting, try setting it through the .macos file

Following these tips will help keep the dotfiles repo up-to-date, enabling the Mac to be restored more easily.