# Gw2 Marker Pack DTD

### What does it do?
Adds custom syntax, validation and autocomplete to your editor

### How to Use:
- Load up your marker pack folder in visual studio code
- Install the VSC extension "XML" by RedHat
- Add the following line at the top of your pack xml to use the dtd:

`<!DOCTYPE OverlayData PUBLIC "" "https://raw.githubusercontent.com/xrandox/Gw2_Marker_Pack_DTD/main/MarkerPack.dtd">`

- That's it! VSC should pull the DTD from the url and apply it to your XML.

### I Use Slightly Different Syntax (CamelCase etc)
You are more than welcome to download the dtd and edit the attributes to fit your current structure. Just drop the .dtd file in the same folder as your marker pack XML and reference it directly with the following line, instead of the PUBLIC line above:

`<!DOCTYPE OverlayData SYSTEM "MarkerPack.dtd">`
