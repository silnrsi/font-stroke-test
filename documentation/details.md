# Details of glyph stroke examples

## Issues

- **Editability** - However the strokes are defined, it is a great advantage to maximise the ease by which designers can edit the strokes in their favourite design app (commonly Glyphs these days). There are two situations where this can be an issue:
    - **Open contours** - In Glyphs, an open contour appears as a simple thin stroke in the preview pane and in the overall Font view, as if you were editing the extreme light weight of a family. If, however, you close the contour, as in an 'o', then it gets filled and it becomes a big black blob. It's then difficult to judge the size and shape in the context of the rest of the glyphs. In addition, any open contours that pass through the blob effectively disappear. Glyphs has a 'Fill Preview' menu option which controls the preview but not the main Font view. The solution is to never quite close a contour, leaving a single unit between the beginning and end of the stroke. However that can also leave tiny imperfections in the expanded stroke.
    - **Dots** - A contour consisting of a single point (typically a dot) is visible when looking at the unexpanded outline, but does not show up at all in the Glyphs preview pane or the Font view. However if you instead replace the single node with a small circle (open or closed) then it becomes visible. And when comparing expanded dots vs. curves, a dot must be slightly larger than the width of a stroke to be balanced in weight, so the small circle technique has other advantages.

## Individual glyph example details

For ease of development, these examples use common glyph names and Unicode values, however there is no intent to make the glyphs match up directly with those definitions. The following table provides details on all the glyphs in the font and their purpose.

Some of these ought to cause no difficulty at all for stroke expansion and dotted/dashed versions. Others push the limits of what can reasonably be expected from a tool.

name|description
----|-----------
a|single line
b|single curve
c|single node; See above note on editability.
d|small circle; See above note on editability.
e|small open circle; See above note on editability.
f|large oval; Similar to an italic 'o'.
g|large open oval; Alternate 'o' technique.
h|left stem; Has with segment and arc, used as component 1.
i|right arch; Used as component 2.
j|right descending hook; Used as component 3a
k|right descending hook overlapping; Used as component 3b
l|'n' shape; Components 1 + 2, touching perfectly.
m|eng; Components 1 + 2 + 3a, with shared end/begin points on 2/3a and a common direction. Has slight risk of showing imperfection in join.
n|eng overlapping; Components 1 + 2 + 3c, with 2 and 3c overlapping. Less chance of break in stroke, but potential disasterous for dotted/dashed lines.
o|eng dereferenced; Same as eng but with components dereferenced. 
p|eng overlapping dereferenced
q|overlapping closed circles (f+f)
r|overlapping open circles (g+g)
s|'o' with bar; Stroke crossing through closed contour.
t|'o' open with bar; Stroke crossing through open contour.
u|'v'; Sharp corners.
v|'v' disconnected; Separate contours meeting in single point with non-common direction (cross reference eng).
w|'w'; Slightly tight angles.
x|'x'; Crossing strokes.
y|'x' compressed; Crossing strokes with tight angles.
z|zigzag; Tightening angles.
A|single-storey 'a' with no overshoot; The top/bottom of the curve is at the same height as the ends of the stem. This is the easiest way to define glyphs that will have extended rounded ends, but a possible problem if the end is a cap or mitre and the expanded stroke is thick.
B|cursive 'v'; Has tight curves that have caused difficulty in stroke expansion, as the inside of the continuous curve must become a sharp corner, and the curve is only minimally defined.
C|cursive 'v' adjusted; Same but with more open curves and inflection control points. This is how I've worked around earlier problems, but not always a reasonable fix.
D|cursive 'r'; Tricky sharp point in upper right that has been troublesome for other tools.
space|space

