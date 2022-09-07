# VHS

GIFs as code. Record GIFs for terminal applications with a just few lines of code 🎬.

<img width="400" src="./examples/demo.gif" alt="Automatic GIF recording with vhs" />

The above example is generated from a single tape file: ([demo.tape](./examples/demo.tape)).

## Tutorial

Type anything into the terminal with the `Type` command.

```
Type "echo 'Hello, world!'"
```

Press the Enter key with the `Enter` command.

```
Enter
```

Press the Backspace key in the terminal with the `Backspace` command.

```
Backspace
```

Wait for a certain amount of time with the `Sleep` command.

```
Sleep 1s
```

Putting it all together...

```
Type "echo 'Hello World'"
Enter
Backspace 5
Sleep 1s
```

Save the above text to a file (`demo.tape`) and generate the GIF with `vhs`:

```bash
vhs < demo.tape
open out.gif
```

<img width="400" src="./examples/tutorial.gif" alt="Tutorial GIF recording with VHS" />

## Commands

* [`Set <Setting> Value`](#settings)
* [`Sleep <time>`](#sleep)
* [`Type "<characters>"`](#type)

### Keys

Key commands take an optional `@time` and repeat `count`.
For example, the following presses the `Left` key 5 times with a 500 millisecond delay between each keystroke.

```
Left@500ms 5
```

* [`Backspace`](#backspace)
* [`Ctrl`](#ctrl)
* [`Down`](#down)
* [`Enter`](#enter)
* [`Left`](#left)
* [`Right`](#right)
* [`Space`](#space)
* [`Tab`](#tab)
* [`Up`](#up)

### Settings

* [`Set FontSize <Number>`](#set-font-size)
* [`Set FontFamily <String>`](#set-font-family)
* [`Set Height <Number>`](#set-height)
* [`Set Width <Number>`](#set-width)
* [`Set LetterSpacing <Float>`](#set-letter-spacing)
* [`Set LineHeight <Float>`](#set-line-height)
* [`Set Theme <String>`](#set-theme)
* [`Set Padding <Number>[em|px]`](#set-padding)
* [`Set Framerate <Number>`](#set-framerate)
* [`Set Output <Path>`](#set-output)

### Sleep

The Sleep command allows you to continue capturing frames without interacting with the terminal.
This is useful when you need to wait on something to complete while including it in the recording like a spinner or loading state.
The command takes a time argument with optional units (`s` or `ms`) by default the units are in `ms`.

```
Sleep 2s
Sleep 500ms
Sleep 2000
```

### Type

The `Type` command allows you to type in the terminal and emulate key presses.
This is useful for typing commands or interacting with the terminal.
The command takes a string argument with the characters to type.

```
Type "echo 'Beep'"
Type "Meow"
```

## Feedback

We’d love to hear your thoughts on this project. Feel free to drop us a note!

* [Twitter](https://twitter.com/charmcli)
* [The Fediverse](https://mastodon.technology/@charm)
* [Slack](https://charm.sh/slack)

## License

[MIT](https://github.com/charmbracelet/vhs/raw/main/LICENSE)

---

Part of [Charm](https://charm.sh).

<a href="https://charm.sh/"><img alt="The Charm logo" src="https://stuff.charm.sh/charm-badge.jpg" width="400" /></a>

Charm热爱开源 • Charm loves open source
