This is a modified version of https://github.com/vishless/dvorak-programmer-mod

# Installation

PLEASE MAKE A BACKUP OF THE FILES BEFORE EDITING

Add the new layout to the symbols directory
Open `/usr/share/X11/xkb/symbols/us` and add the symbols from file `qwerty-programmer-mod` under Dvorak Programmer

Update evdev by opening `/usr/share/X11/xkb/rules/evdev.xml`

And add the following
```
<variant>
    <configItem>
        <name>rdvp</name>
        <description>English (Real Programmer QWERTY)</description>
        <vendor>MichaelPaulson</vendor>
    </configItem>
</variant>
```
To permanently set the layout  
Edit `/etc/default/keyboard` and set the following

```
...
XKBLAYOUT="us"
XKBVARIANT="rpql"
...
```