# eng-cards

## Vim

### Avoiding the Escape Key

Regularly reaching for the escape key in Vim can lead to pinky strain (ouch)!
Remap  to avoid the stretching  and keep your fingers on the home row.

    :imap jj

This allows you to press `jj` to exit from insert mode.  The `:imap` command is
used to create the mapping so that it only applies while in insert mode.  The
pair of characters "jj" occurs very rarely in English, so using it won't
interfere with normal typing

To type "jj" without triggering escape, just wait a couple seconds between each
character.

[VimTips Wiki](http://vim.wikia.com/wiki/Avoid_the_escape_key)

### Instantly preview Markdown from Vim

Want to instantly preview finnicky markdown files, but don't want to leave your
favorite editor, or have to do it in some crappy browser textarea?
**vim-instant-markdown** is your friend! When you open a markdown file in vim, a
browser window will open which shows the compiled markdown in real-time, and
closes once you close the file in vim.

As a bonus,
[github-flavored-markdown](http://github.github.com/github-flavored-markdown/)
is supported, and styles used while previewing are the same as those github
uses!

![Screenshot](http://dl.dropbox.com/u/28956267/instant-markdown-demo_thumb.gif)

[vim-instant-markdown on GitHub](https://github.com/suan/vim-instant-markdown)

### Use a Vim-style editor in XCode

Sometimes IDEs are a necessary evil.  For OO languages and large APIs
or codebases, they can be especially useful.  And XCode has some great features
for building stunning UIs.  But you don't have to give up your the speed and
efficiency of your favorite editor, Vim!

![screenshot](http://cdn-ak.f.st-hatena.com/images/fotolife/g/griefworker/20131101/20131101202840.png)

Install the **XVim plugin** and get a rich set of vim features and keybindings
right inside XCode's editor.

[XVim on GitHub](https://github.com/XVimProject/XVim)

## Manage Vim plugins with Vundle

Automatically manage all of your vim plugins and scripts with Vundle, a plugin
manager for Vim.  Gone are the days of manually downloading, extracting and
installing files into `~/.vim`.  Vundle makes installing, updating and
configuring all your plugins simple.  Just refer to each plugin's GitHub repo in
your `~/.vimrc`

![vundle-installer-screenshot](http://i.imgur.com/Rueh7Cc.png)

## Swift

### Range Operators

Use the range operators to simplify for loop syntax.  You can keep an index in a
loop—either by using `..<` to make a range of indexes or by writing an explicit
initialization, condition, and increment. These two loops do the same thing:

    var firstForLoop = 0
    for i in 0..<4 {
      firstForLoop += i
    }
    print(firstForLoop)

    var secondForLoop = 0
    for var i = 0; i < 4; ++i {
      secondForLoop += i
    }
    print(secondForLoop)


Use `..<` to make a range that omits its upper value, and use `...` to make
a range that includes both values.

[Swift Language Guide](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID60)

## Projects

### Make a programmable mirror

<img src="https://raw.githubusercontent.com/HannahMitt/HomeMirror/master/design/IMG_20150825_191621.jpg" width="400">

Mount an Android device on the back of a two-way mirror to display date,
time, weather, birthday reminders, chore reminders, stock prices, XKCD, etc.

[HomeMirror on GitHub](https://github.com/HannahMitt/HomeMirror)
