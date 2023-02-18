# Gw2 Marker Pack DTD + XSD

## What do they do?
.dtd and .xsd files are XML schema definitions and allow us to add custom syntax, validation and autocomplete to your editor.

DTD is the older style and doesn't provide as much customizability, but is slightly easier to set up.

XSD is the newer style with more customization (and thus better autocomplete etc) but takes a tiny bit extra to set up.

You only need one or the other. I recommend using the XSD as it provides extra functionality.

## Requirements
- Visual Studio Code
- `XML` extension by RedHat
- A Marker Pack

## How to Use:

### XSD
Replace the `<OverlayData>` tag at the beginning of your XML with the following:
```xml
<OverlayData 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="https://github.com/xrandox/Gw2_Marker_Pack_DTD https://raw.githubusercontent.com/xrandox/Gw2_Marker_Pack_DTD_XSD/main/GW2MarkerPack.xsd"
xmlns="https://github.com/xrandox/Gw2_Marker_Pack_DTD_XSD">
```

### DTD
Above the `<OverlayData>` tag, add the following line:
```xml
<!DOCTYPE OverlayData PUBLIC "" "https://raw.githubusercontent.com/xrandox/Gw2_Marker_Pack_DTD_XSD/main/GW2MarkerPack.dtd">
```

That's it! VSC should pull the XSD or DTD from the url for the extension to use.

## I Use Slightly Different Syntax (CamelCase etc)
While I recommend using the provided syntax for consistency sake, you are more than welcome to download the xsd/dtd and edit the attributes to fit your current structure. Just drop the file in the same folder as your marker pack XML and reference it directly according to which file you use:

### XSD
Replace the `<OverlayData>` tag at the beginning of your XML with the following:
```xml
<OverlayData 	
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:schemaLocation="https://github.com/xrandox/Gw2_Marker_Pack_DTD GW2MarkerPack.xsd"
xmlns="https://github.com/xrandox/Gw2_Marker_Pack_DTD_XSD">
```

### DTD
Above the `<OverlayData>` tag, add the following line:
```xml
<!DOCTYPE OverlayData SYSTEM "GW2MarkerPack.dtd">
```

## There's A Bug With Your Schema
Please feel free to create an issue describing the issue and I'll get to it ASAP! Or, if you are so inclined, feel free to fix the error and create a pull request!



## Credits
Created by
Discord: null#7146

IGN: xTeh.7146
