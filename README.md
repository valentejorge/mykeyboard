# My keyboard layout 

is a abnt2 brazilian keyboard layout with some mods.

![keyboard image](https://github.com/valentejorge/mykeyboard/blob/main/image.jpg)

___
### Install
```
$ cd
$ git clone https://github.com/valentejorge/mykeyboard/
$ cd mykeyboard/
$ sudo cp mykeyboard /usr/share/X11/xkb/symbols/
```
Add the new layout declaration to ```/usr/share/X11/xkb/rules/evdev.xml```
```
...
    <layout>
      <configItem>
        <name>mykeyboard</name>

        <shortDescription>mykb</shortDescription>
        <description>mykeyboard</description>
        <languageList>
          <iso639Id>por</iso639Id>
        </languageList>
      </configItem>
      <variantList>
      </variantList>
    </layout>
...

```
inside a &lt;layoutList&gt; ... &lt;/layoutList&gt;

if you are in the arch/i3, change your `/etc/X11/xorg.conf.d/00-keyboard.conf` to:
```
# Written by systemd-localed(8), read by systemd-localed and Xorg. It's
# probably wise not to edit this file manually. Use localectl(1) to
# instruct systemd-localed to update it.
Section "InputClass"
        Identifier "system-keyboard"
        MatchIsKeyboard "on"
        Option "XkbLayout" "mykeyboard"
        Option "XkbOption" "caps:escape"
EndSection
```
