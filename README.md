OTP Token Paster for OS X
=========================

An OS X service that automatically enters the current one-time password
(OTP) into the current iTerm window.

It doesn't overwrite the contents of the clipboard, and uses the [OATH
Toolkit](http://www.nongnu.org/oath-toolkit/)'s oathtool(1) to generate the
token.


Using
=====

- Install [Homebrew](http://mxcl.github.com/homebrew/)
- ```brew install oath-toolkit```
- If it isn't already present, enter ```secret=YOUR_BASE32_ENCODED_SECRET```
  in ```~/.JAuth.rc```.
- ```mkdir -p ~/Library/Services```
- Clone the repository.
- ```mv 'Enter Current OTP Token.workflow' ~/Library/Services```
- Open System Preferences -> Keyboard -> Keyboard Shortcuts -> Services ->
  Enter Current OTP Token (probably way down at the bottom).
- Click 'add shortcut' and enter the key combination you want to use.


Caveats
=======

The hotkey won't work until you go to the application menu in iTerm (click
'iTerm' in the menu bar) and point at the Services menu. You don't have to
actually click any of the services; expanding the menu is enough to make OS
X recognize the keyboard shortcut exists. You have to do this each time you
run iTerm.

I'm guessing this is a bug in OS X, and displaying the Services menu forces
it to load the service information.
