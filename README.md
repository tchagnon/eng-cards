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

[VimTips Wiki](vim.wikia.com/wiki/Avoid_the_escape_key)

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

[View on GitHub](https://github.com/HannahMitt/HomeMirror)
