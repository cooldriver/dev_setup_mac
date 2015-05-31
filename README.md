# Dev Setup Mac OS X
A guide to setup a development environment on a new Mac.

## Summary

* [System update](#system-update)
* [System preferences](#system-preferences)
* [Dropbox](#dropbox)
* [Browsers](#browsers)
* [iTerm2](#iterm2)
* [1 Password](#1-password)
* [Alfred](#alfred)
* [Vim](#vim)
* [ZSH](#zsh)
* [Homebrew](#homebrew)
* [Inspiration](#inspiration)

## System update

Check if system updates are available (`Apple menu > Software Update...`)

## System preferences

### Change DNS

1. Go to `System Preferences > Network`;
2. Select `Wi-Fi` from the left-hand pane and click the Advanced button;
3. Open the `DNS` tab;
4. Click the + button under the DNS Servers and type `4.4.4.4`;
5. Click the + button (again) and type `8.8.8.8`;
6. Hit `OK`.

You might want to repeat the process for your Ethernet interface.

## Dropbox

* [Link](https://www.dropbox.com/)

## Browsers

### Firefox

* [Link](https://www.mozilla.org/fr/firefox/new/)
* Enable sync
* Extensions:
  * Firebug
  * YSlow
  * ColorZilla
  * DNS Flusher
  * ~~HttpRequester~~ (obsolete, see Postman on Chrome)
  * 1 Password

### Chrome

* [Link](https://www.google.fr/chrome/browser/desktop/)
* Enable sync
* Extensions:
  * Adblock Plus
  * Checker Plus for Gmail
  * Google Cast
  * Hola
  * Postman

## iTerm2

* [Link](https://www.iterm2.com/downloads.html)

## 1 Password

* [Link](https://agilebits.com/onepassword)

## Alfred

* [Link](http://www.alfredapp.com/#download)
* Sync with dropbox
* Workflows:
  * Caffeniate Control

## Vim

* Copy `.vimrc` to `~`

## ZSH

* [Link](https://github.com/robbyrussell/oh-my-zsh)
* Copy `.zshrc` to `~`

## Homebrew

### Installation

First, install XCode, then run the following command.

```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

One thing we need to do is tell the system to use programs installed by Hombrew (in `/usr/local/bin`) rather than the OS default if it exists. As ew use ZSH, we do this by checking if the file `.zshrc` has the following line (it should if you used the dotfile in this repos):

```bash
export PATH="/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
```

Open a new terminal tab with `Cmd+T` (you should also close the old one), then run the following command to make sure everything works:

```bash
$ brew doctor
```

Then update Homebrew's directory of formulae:

```bash
$ brew update
```

## Inspiration

* [nicolashery](https://github.com/nicolashery/mac-dev-setup)
* [jmike](https://github.com/jmike/Mac-OSX-Ninja-Setup)
* [Altryne's Blog](http://alexw.me/2013/10/definitive-guid-to-development-mac-setup/)
* [dotfiles.github.io](http://dotfiles.github.io/)
