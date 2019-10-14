# GMailinator

Adds Gmail-esque keyboard shorcuts to Mail.app.  This is still very much a work
in progress.  Tested with Mail for OS X Catalina.

## Supported Shortcuts

|  Key   | Action                         |
| :----: | ------------------------------ |
|   #    |  Delete                        |
|   /    |  Mailbox search                |
|   !    |  Toggle message as Junk        |
|   a    |  Reply All                     |
|   c    |  Compose new message           |
|  e, y  |  Archive                       |
|   f    |  Forward message               |
|   G    |  Go to the last message        |
|   g    |  Go to the first message       |
|   j    |  Go to next message/thread     |
|   k    |  Go to previous message/thread |
|   l    |  Move to folder (opens dialog) |
|   o    |  Open selected message         |
|   R    |  Get new mail (Refresh)        |
|   r    |  Reply                         |
|   s    |  Flag                          |
|   u    |  Mark message as read          |
|   U    |  Mark message as unread        |
|   v    |  View raw message dialog       |
|   z    |  Undo                          |

## How to install

1. Clone the repository
2. Navigate to it in your terminal
2. Enable Mail.app plugins (stop Mail.app if it's running):
       `defaults write com.apple.mail EnableBundles -bool true`
3. run `xcodebuild` (make sure you actually have xcode installed)
4. run `mv ./build/Release/GMailinator.mailbundle ~/Library/Mail/Bundles`
5. start mail app, open settings -> plugins -> activate it.
6. restart mail app :)

## Credits

A lot of this was built with heavy use of of the
[BindDeleteKeyToArchive](https://github.com/benlenarts/BindDeleteKeyToArchive)
project by Ben Lenarts.  The Xcode project and interface skeleton were
all from that project, and for the most part, renamed.  I added the keybinding code.

A lot of the code is also either copied in whole, or modified from the
Nostalgy4Mail.app project, by [Hajo Nils
Krabbenhöft](https://github.com/fxtentacle/Nostalgy-4-Mail.app), and
subsequently by [Jelmer van der
Linde](https://github.com/jelmervdl/Nostalgy-4-Mail.app). I've added support
for ARC (turns out there were quite a few leaks), and prettied-up (imho) the
move-to-folder dialog.

Other references:

- [Rui Carmo's PyObjC vim keybinding script](http://taoofmac.com/space/blog/2011/08/13/2110)
