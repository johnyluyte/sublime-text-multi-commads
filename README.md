# Sublime Text Multi Commands

A simple python script that enable users to easily execute multiple commands in Sublime Text 3. The original author is **Nilium**, who shared the original python code [here](https://www.sublimetext.com/forum/viewtopic.php?f=5&t=8677).

I made a very tiny change to the code so that it can work with packages like [sublime-evernote](https://github.com/bordaigorl/sublime-evernote).


## Install

Download and put **run_multiple_commands.py** in your `/Packages/User/` directory.

You can find the directory through `Preferences -> Browse Packages` in Sublime Text. Or depending on your OS, you can allocated it at:

OSX

    ~Library/Application Support/Sublime Text 3/Packages

Windows

    C:\Users\epti-215\AppData\Roaming\Sublime Text 3\Packages

Linux

    ~/.config/sublime-text-3/Packages/

## Usage

Open your `sublime-keymap` file from `Preferences -> Key Bindings` in Sublime Text. Add multiple commands like the following examples.

### Save file & Update to evernote

In this example, when the user click "super+s", command *save* and command *save_evernote_note* will be executed.

```json
  {
    "keys": [
      "super+s"
    ],
    "command": "run_multiple_commands",
    "args": {
      "commands": [
        {
          "command": "save"
        },
        {
          "command": "save_evernote_note",
          "context": [
            {
              "key": "evernote_note"
            }
          ]
        }
      ]
    }
  }
```

### Another example:

This is the example provided by **Nilium**.

```json
{
  "keys": [
    "ctrl+w"
  ],
  "command": "run_multiple_commands",
  "args": {
    "commands": [
      {
        "command": "find_under_expand",
        "context": "window"
      },
      {
        "command": "show_panel",
        "args": {
          "panel": "find"
        },
        "context": "window"
      }
    ]
  }
}
```

## Credit

For Sublime Text Multi Commands, credit gose to its original author, **Nilium**.
For [Sublime Evernote](https://github.com/bordaigorl/sublime-evernote), credit goes to its contributors.