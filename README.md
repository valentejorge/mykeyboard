# My keyboard layout 

is a abnt2 brazilian keyboard layout with some mods.

![alt text](https://github.com/jotavev/mykeyboard/blob/main/image.png)

this is not a final version, but...
___
### Install
```
$ cd
$ git clone https://github.com/jotavev/mykeyboard/
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
