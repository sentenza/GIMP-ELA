JPEG Error Level Analysis for the GIMP
======================================

The JPEG-compression is a lossy technique. The use this compression on digital images introduces an error on each block of 8x8 pixels that composes the resulting imag. However, when an image is modified, the 8x8 cells containing the modifications have no longer the same error level of the rest of the unmodified image.

The Error Level Analysis (ELA) aims to discover areas within a JPEG image that are at different compression levels, so that a possible manipulation of the highlighted portions could be clued. In order to succeed in this operation the original image is intentionally resaved at a known error rate (such as 70%) and then the difference between the resulted image and the original one is computed. If an area of the image has been compressed multiple times one could suppose that the image has possibly been manipulated.


Installation
------------

In order to install this Python plugin in GIMP (tested with GIMP 2.8+) you must save *plugin-ela.py* under the plug-ins directory and then start the GIMP. The new _Forensics_ submenu would be disposable under _Filters_.

Usage
-----

After selecting the JPEG ELA plugin from _Filters_ on a saved JPEG image it is possible to specify the amount of compression of the resaved image and an HTML report.


### Requirements

# GIMP 2.8+
# Python
