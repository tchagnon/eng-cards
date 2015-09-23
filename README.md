# eng-cards

**Table of Contents**

<!-- To update Table of Contents:
  npm install -g doctoc
  doctoc README.md -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Vim](#vim)
  - [Avoiding the Escape Key](#avoiding-the-escape-key)
  - [Instantly preview Markdown from Vim](#instantly-preview-markdown-from-vim)
  - [Use a Vim-style editor in XCode](#use-a-vim-style-editor-in-xcode)
  - [Manage Vim plugins with Vundle](#manage-vim-plugins-with-vundle)
  - [Toggle paste mode with \p](#toggle-paste-mode-with-%5Cp)
- [Swift](#swift)
  - [Range Operators](#range-operators)
- [Projects](#projects)
  - [Make a programmable mirror](#make-a-programmable-mirror)
  - [Command Line Pandora Client for Mac](#command-line-pandora-client-for-mac)
- [cURL](#curl)
  - [Word Definitions from the Command Line](#word-definitions-from-the-command-line)
  - [Customize cURL's Output](#customize-curls-output)
- [Open Source Projects](#open-source-projects)
  - [Neovim - Next Generation Vim Text Editor](#neovim---next-generation-vim-text-editor)
  - [CockroachDB - Google Scale for the Masses](#cockroachdb---google-scale-for-the-masses)
- [Android](#android)
  - [Retrieve System Logs from Your Device](#retrieve-system-logs-from-your-device)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

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

### Manage Vim plugins with Vundle

Automatically manage all of your vim plugins and scripts with Vundle, a plugin
manager for Vim.  Gone are the days of manually downloading, extracting and
installing files into `~/.vim`.  Vundle makes installing, updating and
configuring all your plugins simple.  Just refer to each plugin's GitHub repo in
your `~/.vimrc`

![vundle-installer-screenshot](http://i.imgur.com/Rueh7Cc.png)

[Vundle on GitHub](https://github.com/VundleVim/Vundle.vim)

### Toggle paste mode with \p

Auto-indenting, key mappings and other settings can mess up the formatting and
indentation when pasting code into Vim.  To avoid this problem, Vim provides a
paste mode that turns these features off in insert mode.  To enable or disable
paste mode:

    :set paste
    :set nopaste

[![vim-paste](images/vim-paste.gif)](https://asciinema.org/a/26660?autoplay=1)

Binding a fast key sequence to `pastetoggle` will make it quick and easy to turn
`paste` mode on and off.  For example, put the following in your `.vimrc`:

    set pastetoggle=<Leader>p

`<Leader>` defaults to the backslash `\` character if you don't have a custom
[mapleader](http://usevim.com/2012/07/20/vim101-leader/) set.
To use this, enter insert mode, then type the `\` and `p` keys sequentially.
You should see:

    -- INSERT (paste) --

and be able to paste without broken formatting.  Type `\` `p` again to turn off
paste mode.

[VimTips Wiki](http://vim.wikia.com/wiki/Toggle_auto-indenting_for_code_paste)

### Turn on line numbering

Line numbers can be very important to using vim effectively.  Most normal mode
commands take optional line number or repeat count.  For example, `8gg` will jump
to line 8.  To turn on and off line numbers use:

    :set number
    :set nonumber

It can also be helpful to set a different color scheme for the line number
columns to clearly distinguish them from the buffer text.

    :highlight LineNr ctermfg=black ctermbg=gray

Some commands work better with relative line numbers.  Typing `3j` will move
down by 3 lines from the current position, or `4dd` will delete 4 lines.  For
these, it can be helpful to set relative line numbering:

    :set relativenumber

![vim-number](images/vim-number.gif)

[VimTips Wiki](http://vim.wikia.com/wiki/Display_line_numbers)

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

###Command Line Pandora Client for Mac

Skip the ads without upgrading and more importantly free yourself from the unnecessary bloat of a GUI. That's right a simple but powerful command line Pandora Client in less than two minutes. 

Step one: Install Homebrew (you'll thank us later)

    curl -L http://github.com/mxcl/homebrew/tarball/master | tar xz --strip 1 -C /usr/local

Step two: Install Pianobar

    brew install pianobar

Step three: Run Pianobar


    pianobar

<img src="http://s7.postimg.org/6mxhmjbob/pandora_command.gif" width="400">

## cURL

###Word Definitions from the Command Line

You can use cURL to get the definition for a word with the help of the DICT protocol. Just pass a Dictionary Server URL to it and the word you want the definition for. 

    $curl dict://dict.org/d:genesis

The above command will list the definition for genesis as follows: 

    "genesis" gcide "The Collaborative International Dictionary of English v.0.48" Genesis \Gen"e*sis\, n. [L., from Gr. ge'nesis, fr. the root of gi'gnesqai to geget, be born; akin to L. genus birth, race. See {Gender}. ]

    [1913 Webster]

    1. the act of producing, or giving birth or origin to anything. 

###Customize cURL's Output

Normally, when you use cURL you use the command

    $curl -IL "url"

The above command would send a HEAD request (-I), follow all redirects (-L), and display some useful information: 

    HTTP/1.1 200 OK
    Date: Mon, 14 Sep 2015 08:57:17 GMT
    Expires: -1
    Cache-Control: private, max-age=0
    Content-Type: text/html; charset=ISO-8859-1
    P3P: CP="This is not a P3P policy! See http://www.google.com/support/accounts/bin/answer.py?hl=en&answer=151657 for more info."
    Server: gws
    X-XSS-Protection: 1; mode=block
    X-Frame-Options: SAMEORIGIN
    Set-Cookie: PREF=ID=1111111111111111:FF=0:TM=1442221037:LM=1442221037:V=1:S=0D6fmKXKZeC7wtqi; expires=Thu, 31-Dec-2015 16:02:17 GMT; path=/; domain=.google.com
    Set-Cookie: NID=71=XvDbVOyhmtTu7Un1KojuMxqXI6moknK_u-OIBlVZ8sbtsYZ8HotHRryJoPAyOP4Wo6fFLZgHIfyL8isO4wIrIM_rgmTExQ_dHIwJrpsfyaJTs-XYxPclnIAammkjtP6K; expires=Tue, 15-Mar-2016 08:57:17 GMT; path=/; domain=.google.com; HttpOnly
    Transfer-Encoding: chunked
    Accept-Ranges: none
    Vary: Accept-Encoding

But what if you're only interested in a subset of the standard cURL output? cURL provides special variables for customizing output. The following command only prints the http status code of the request and redirects curl's HTML output to /dev/null. 

    $curl -sL -w "%{http_code} % {url_effective} \\n" "URL" -o /dev/null

The above command results in the following output: 

    200 HTTP://www.google.com/

Here are the other special variables available in case you want to customize the output some more. 

    url_effective, http_code, http_connect, time_total, time_namelookup, time_connect, time_pretransfer, time_redirect, time_starttransfer, size_download, size_upload, size_header, size_request, speed_download, speed_upload, content_type, num_connects, num_redirects, ftp_entry_path

##Open Source Projects

###Neovim - Next Generation Vim Text Editor

The Vim text editor has been loved by a generation of users. We're aggressively refactoring Vim to ensure it stays relevant in the future. 

**More Powerful Plugins**

Neovim is rebuilding the plugin architecture from the ground up to provide a system that allows for extensions in any language and will be backwards compatible with your old plugins. 

**Better GUI Architecture**

Neovim will focus on providing a headless text editing environment. This will allow any GUI to be written that ties into the native GUI of whatever os it is running on. 

**First Class Support for Embedding**

Any program will be able to include NeoVim commands right in the application. 

![Screenshot](https://raw.githubusercontent.com/junegunn/i/master/vim-plug/nvim.gif)

[neovim on GitHub](https://github.com/neovim/neovim)

###CockroachDB - Google Scale for the Masses

Finally, a db as indestructible as a cockroach. While at Google we fell in love with Spanner, Google's solution to juggling data between millions of database servers, so we decided to create an open source project to bring that scalability to the masses. 

**Automated Scaling / Repair**

CockroachDB will allow you to add resources to scale horizontally, with zero hassle and no downtime. It will self-organize, self-heal, and automatically rebalance.

**Strong Consistency**

CockroachDB will implement consistent replication via majority consensus between replicas. 

**Distributed Transactions**

CockroachDB will implement efficient, full-serializable distributed transations. 

[CockroachDB on GitHub](https://github.com/cockroachdb/cockroach)

##Android

###Retrieve System Logs from Your Device

When your application crashes and the device isn't connected to a computer you still need the system logs to uncover what went wrong and luckily there's a really powerful and free tool for that called Android Debug Bridge (adb). 

In order to use adb with a device connected over USB, you must enable USB debugging in the device system settings under Developer options. 

Open your terminal and navigate the Android skd sub directory platform-tools type in the following command to dump the log to the screen. 

    $adb logcat -d 

The command above will produce the following output: 

    
