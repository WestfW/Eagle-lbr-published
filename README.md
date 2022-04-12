# Eagle-lbr-published
User-language-programs (ULPs), scripts, and libraries for CadSoft EAGLE's Schematics/PCB editor

----

### eagle.scr<br> billw-brd.scr<br>billw-lbr-dev.scr<br>billw-lbr-pac.scr<br>billw-lbr-sym.scr<br>billw-sch.scr
These are the auto-running scripts I use.   Mostly, they add some menu commands that I find useful to the various EAGLE editors.  (For example, some "layers" shortcuts appropriate for each editor.)

### circle.ulp<br>circle2.ulp
Draw circles (on the current layer) with a user-specified diameter.  At the origin (they can be moved, afterward.)  circle2 draws the circle as a polygon rather than as a built-in circle, which means it can be filled.

### classes.ulp
Sets signal classes (trace widths), if they're not already set.

### convexshell.ulp
An experiment in implementing the "Convex shell" algorithm around a set of points drawn on a board.  It does work, but I'm not sure it's useful.  In theory, this provides an easy way to generate complex board outlines.  It does demonstrate the implementation of more complex algorithmic code in the EAGLE C-like extension language.

default-outlines.scr

### del-optional-layers.ulp
Sometimes boards wind up with a bunch of user- or maybe library-defined layers that aren't in use.  Probably when a library includes imported bitaps.  This script deletes them.

### oshw-logo.ulp
Draw a OSHW logo on the board with a particular diameter, at the current mark.  Best to have that mark be off in a blank space, and then manually moved to where you want it.  Logo is drawn on TOP and TPLACE.

### protoboard.ulp
Lay out a set of vias and traces to implement an arbitrary-sized "protoboard" area on your board.

### smash_all.ulp
"smash" all the devices/packages on a schematic or board.  "Smashing" dissociates the package name and value, so that they can be moved separately from the package outlines.  Useful for cleaning up silkscreens.

### silk-new.ulp
My version of the silkscreen re-drawing script.  Redraws most silkscreen objects on a new layer, usually with increase line widths in order to meet PCB maker requirements.   Once you have the separate layer, you can edit it extensively since the objects are no longer sub-parts of a package/etc, and make your silkscreens much prettier.  (remember to use the new layers when output gerbers!)

### gridhalf.ulp<br>toglay.ulp<br>toglays.ulp<br>rippoly.ulp
Designed to be used from menus.  Ie, you create menu buttons to halve or double your grid size, and they do "run gridhalf.ulp ..." with appropriate parameters.  ULPs are generally needed to access internal information that scripts and menus do not have access to (like "current grid values.")

### ps-drillaid.txt
This gets added to eagle.def to define a new CAM output device that is postscript with the "holes" in pad all shrunken, similar to the "drill-aid" ULP but for CAM output rather than just printing.  Um.  I don't remember why I needed this. :-( (There's probably a discussion in the CADSOFT forums, if they were preserved though the multiple acquistitions.)

### dynframe.ulp
Draw a dynamically size frame around your schematic.  Useful when you're goin to use the "magnification" feature of printing rather than expecting every drawing to fit on a fixed-size page.

--

import-text.ulp<br>
lbrutil.ulp<br>
ledarray.ulp<br>
listlbrs.ulp<br>
ls.ulp<br>
menu.ulp<br>
menu_util.ulp<br>
newboardtest.ulp<br>
parabolic.ulp<br>
pinnames.ulp<br>
pinpoly.ulp<br>
segmented-ring.ulp<br>
showclass.ulp<br>
showsigs.ulp<br>
textexport.ulp<br>
upline.ulp<br>
I don't know if any of these are generally useful.  It looks like I uploaded a bunch of files to githib without paying much attention to how "developed" either the code or the use-cases were.
