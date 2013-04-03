Illustrator to Edge Animate exporter
---------

>WARNING: This is an early preview for an upcoming (unofficial) panel / extension. This script will modify the original .an file so please backup and use at you own risk!

[DOWNLOAD THE SCRIPT](https://raw.github.com/davidderaedt/CSscripts/master/illustrator/export2EdgeAnimate/export2Animate.jsxbin)

This script exports the active Illustrator document to an Edge Animate project. Each layer is converted to a SVG or PNG file (the export type option is at the end of the script) placed in the project's "images" folder. The project's `xxx_edge.js` dom array will also be modified to properly place each image onto the project's stage.

Note that only top level layers are exported. Each layer's content is flattened to a bitmap (PNG24) or vector (SVG) data, whatever its content. If your file doesn't use layers, consider using my `distributeSelectionToLayers.jsx` script which does exaclty that.


Known Issues

* Hidden layers will be ignored by the animate project but still exported in the image folder
* SVG export is slow, much slower than PNG.

Possible roadmap

* Symbols conversion (AI symbol to Animate symbol)
* Optionnaly export artboard size to stage size
* Optionnaly export in a div/group
* Allow sub-layers / sub-items grouped into divs/groups
* … your idea go here !