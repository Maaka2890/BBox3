# BoundingBox QGIS 3 Plugin
This QGIS 3 plugin returns the xmin, ymin, xmax, ymax and the GetMap request of the current view window of the selected WMS.

Developers of web services often need bounding boxes of specific areas during trouble shooting, for test calls or for communication. 
The goal of this plugin is to, with one click, provide the bounding box of the current view window and the GetMap request of the selected WMS. You can copy this for your tests. 
With this plugin you can pan to a new location and press "Get BBOX" to updated the bounding box and GetMap request. Making it the quickest way of getting the needed information. 
No more need for different software, python commands, or copying xmin, ymin etc. one by one. Your bounding box is only 2 clicks away. 

Notes:
Put the content in a folder called "BoundingBox" in C:\Users\\[USERNAME]\\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins.
The GetMap request only works if you use the English Qgis. The plugin searches metadata therms which, when translated, can't be found. You can change the locale by going to Settings->Options|Locale and use U.S. English.
It also only returns the GetMap request if you select (highlight) the WMS in the Layers Panel.
The order will be xmin, ymin, xmax, ymax. This corresponds to the gml simple features point geometry encoding. Depending on the EPSG code you might need ymin, xmin, ymax, xmax in your tests.

This plugin was created using Plugin Builder 3, Qt Designer and python. 
For more information, see the PyQGIS Developer Cookbook at:
https://docs.qgis.org/3.4/en/docs/pyqgis_developer_cookbook/index.html

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.