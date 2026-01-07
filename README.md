# BoundingBox QGIS 3/4 Plugin
This QGIS 3/4 plugin returns the xmin, ymin, xmax, ymax and the GetMap request of the current view window of the selected WMS.

Developers of web services often need bounding boxes of specific areas during trouble shooting, for test calls or for communication.  
The goal of this plugin is to, with one click, provide the bounding box of the current view window and the GetMap request of the selected WMS. You can easily copy this for your tests. Making it the quickest way of getting the needed information.  
No more need for different software, python commands, or copying xmin, ymin etc. one by one. Your bounding box is only 2 clicks away. 

- pan to a new location 
- open de BBOX plugin
- press "Get BBOX" to updated the bounding box and GetMap request. 

## Install notes:  
This plugin is available trough the Plugin manager inside Qgis.

Install from github:
- Put the content in a folder called "BoundingBox" 
- zip 
- in Qgis open mode Plugin manager and import from zip. 

OR
- Put the content in a folder called "BoundingBox" in C:\Users\\[USERNAME]\\AppData\Roaming\QGIS\QGIS[version]\profiles\default\python\plugins.

## Troubleshooting 
###  AttributeError
The GetMap request only works if you use the English Qgis. The plugin searches metadata therms which, when translated, can't be found.  
You can change the language by:
- go to Settings:
- Options | Locale and use U.S. English.

### GetMap box empty
It only returns a GetMap request if you select (highlight) the WMS in the Layers Panel. 

### Bounding boxes representation
The order will be xmin, ymin, xmax, ymax. This corresponds to the gml simple features point geometry encoding. Depending on the software you might need ymin, xmin, ymax, xmax or another order in your tests.  
cheetsheet: https://github.com/perrygeo/bbox-cheatsheet/blob/master/reference.md

## Acknowledgments

This plugin was created using Plugin Builder 3, Qt Designer and python. And upadted to Qt6 using <https://github.com/qgis/QGIS/wiki/Plugin-migration-to-be-compatible-with-Qt5-and-Qt6>  
For more information, see the PyQGIS Developer Cookbook at:
https://docs.qgis.org/3.4/en/docs/pyqgis_developer_cookbook/index.html

## License
This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.