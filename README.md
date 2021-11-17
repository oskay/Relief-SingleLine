# Relief Single Line

*Relief SingleLine* is a versatile sans serif “single-line” font with open paths oriented towards CNC (Computer Numerical Control) engraving and fab labs environment. *Relief SingleLine* provides a single-line path for a pen, laser, or milling tool to follow for an efficient and clean looking typographical rendering. *Relief SingleLine* has a “classic” outlined companion, [*Relief*](https://github.com/isdat-type/relief), for print and screen environments.

## Existing CNC mill & laser typographic tools
Nowadays there is still a critically small amount of “single-line”, “single-stroke” or “central-line” fonts optimized for fab labs CNC machinery, allowing the use of letters based on a single central line. Simultaneously, typographic tools dedicated to CNC usages (such as [Hershey Text](https://wiki.evilmadscientist.com/Hershey_Text) extension on Inkscape) are truly limited and the drawing quality of the proposed fonts doesn’t match current typographic standards. The existing offer (both commercial and open-source) of single-line fonts is very basic and the majority of these available typefaces are qualitatively deceptive (irregular drawing quality, poor spacing, no kerning, etc.). With the recent variable fonts technology, the type design field is currently in a boom, but strangely the rapidly democratizing domain of fab labs is hardly approached by type designers. This potential space for experimentation is practically left to engineers and “makers” which, despite all their noticeable efforts, need more typographic expertise and the help of the type design community.

## Relief SingleLine, a skeletal font for CNC machinery
*Relief SingleLine* is a versatile sans serif “single-line” font with open paths designed by students of the Graphic Design Department of the Institut Supérieur des Arts et du Design de Toulouse / [isdaT](https://www.isdat.fr/) (Élisa Garzelli & Noëlie Dayma). The project was initiated and led by François Chastanet (isdaT Graphic Design Department teacher) part of *Les Communs / Bibliothèque Infinie* pedagogical program curated by Nathalie Bruyère (isdaT Design Department teacher). The structure of this alphabet is influenced by Adrian Frutiger’s little known and underrated Vectora typeface. Relief SingleLine comprises an additional ornamental geometric set matching with both uppercases and lowercases’ heights. 

*Relief SingleLine* allows the user to drastically reduce the machining time while offering a quality Bézier curves rendering. The Relief project is based on a main skeletal .glyphs source and explores different font format exports: 

— Open Path / CNC machining
• OTF-SVG for Adobe,
• UFO for Fontlab Pad and Drawbot, 
• SVG for Inkscape + Hershey Text Extension,
• Closed TTF and Stick TTF for CAD softwares (like Rhinoceros 3D or CamBam).

— Classic Closed Outlines / Print and Web
• OTF (the closed outlines OTF version is necessary in the first steps of the Inkscape layout process)
• WOFF

When using *Relief SingleLine* font with a laser-cutting machine, it is recommended to use the *cutting* function at low intensity and not the *engraving* function in order to reduce inscription’s tracing time on any surface (do preliminary laser power tests to determine the best speed / power couple for each material to engrave with an inscription).


## How to use it?

### AdobeCC ≥2019: OpenType-SVG color font method
As this project is primarily focusing on graphic user interface solutions opened the largest possible audiences, *Relief SingleLine* font is distributed as an OpenType-SVG color font format in order to simplify the 2D layout process for the 2D fab lab community, i.e. having a central-line font editable in popular vector graphics and typographic softwares such as Illustrator or Indesign. OpenType-SVG technology represents an interesting alternative to permit single-line fonts wider distribution and easier use. To our knowledge, *Relief SingleLine* is the first single-line font working in the Adobe CC environment (CC 2019 and above), opening new perspectives for makers worldwide. Fab lab users oriented towards 2D graphic practices can now easily access quality Bézier curves, kerning and OpenType features in their single-line typographical layouts!

Simply install the “Relief SingleLine-Regular_svg.otf” on your system (or directly in the /Fonts subfolder of Illustrator or Indesign), open Illustrator or Indesign, compose your paragraphs and titlings; when the layout is finished, duplicate it and just use the /Text/Vectorize function (shift+command+O) to obtain a single-line design to export as PDF or SVG file to engrave through your favorite CNC machine (pen plotters, laser cutting or milling machine).

*Relief SingleLine* export as OpenType-SVG format was made possible thanks to [Frederik Berlaen](https://typemytype.com/)’s *otf-svgMaker* Python script for [Robofont](https://robofont.com/). This script permits to export any skeletal UFO-based font project towards an single line OTF-SVG font. *otf-svgMaker* uses [roundingPen](https://github.com/typemytype/outlinerRoboFontExtension/blob/master/Outliner.roboFontExt/lib/outlinePen.py) script by Jost Van Rossum. *otf-svgMaker* will be soon available in this repository.

#### →fonts/AdobeCC/

### FontLab Pad or Drawbot method / UFO
UFO format ([Unified Font Objects](https://unifiedfontobject.org/)) is a cross-platform, cross-application, human readable format for storing font data. Download the Relief UFO file, open it with [FontLab Pad](https://www.fontlab.com/fontlab-pad/) text editor (free of use, available for Windows and Mac), type your text, then export it as an PDF or SVG composition that you can open in any vector graphics software, run CNC. The UFO file can also be used in [Drawbot](https://www.drawbot.com/) to export towards PDF or SVG textual vector patterns to engrave. 

#### →fonts/FontlabPad+Drawbot/

### Inkscape / Hershey Text Extension SVG fonts method

First install Relief-SingleLine-Regular.otf on your system, then parallelly copy Relief-SingleLine-Regular.svg there: (macOS) Applications / Inkscape (show package content) / Contents / Resources / share / inkscape / extensions / svg_fonts / Relief-Regular.svg. 

Compose your layout in [Inkscape](https://inkscape.org/) using Relief-SingleLine-Regular.otf, launch [Hershey Text Extension](https://www.evilmadscientist.com/2019/hershey-text-v30/) (now available by default) to render your text blocks as single-line letters: go to Extension / Text / Hershey Text, in font select *Other* (bottom of the list after the existing Hershey fonts) and type Relief-SingleLine-Regular in the next field of the dialog box as a path / name, then apply rendering. 

Beware to first copy your source text blocks: after the Hershey Text Extension rendering process, texts are becoming not editable. Contrary to the Fontlab Pad method, Hershey Text extension unfortunately apparently disables the kerning values even if truly embedded in the SVG font.

#### →fonts/Inkscape/

Process to export towards (old) SVG format with open paths (thanks to Tanguy Vanlaeys):

• Open UFO file in Fontforge, export as SVG;

• Open the SVG file in a text editor (such as Sublime Text) and run two find & replace actions:

— find z" /
— replace by " /

— find zM
— replace by M

• Save as new SVG file.


### CAD softwares: Closed TTF + Stick TTF fonts 
[Rhinoceros 3D](https://www.rhino3d.com/) and some other CAD softwares are able to use closed TTF single-line fonts by opening the closed contours the right way in its design interface with various views. When operating the text tools dialog box you have a special feature to tick to permit single-line fonts usage (Windows version only in Rhino 3D); select the desired TTF. But composing paragraphs is often not possible, you can just write some words aligned on the same baseline (no line breaks depending on softwares), so limited to basic titling usages only.

A «stick» font is composed of an original path that is duplicated to close it — the second lines go directly on top of the originals. We propose here both a triangular closed TTF font and a closed stick TTF font.

#### →fonts/CAD-softwares/ttf-closed+stick

## Typographic engraving proofs

First laser engraving tests on plywood at various speeds and laser powers, [Artilect](https://artilect.fr/) fablab, Toulouse, 2021 / 03 / 23.

![](/documentation/images/photos/relief_laser_2021_03_25_a.jpg)
![](/documentation/images/photos/relief_laser_2021_03_25_b.jpg)

## Contributors

Élisa Garzelli & Noëlie Dayma, isdaT Graphic Design Department students.

[François Chastanet](http://francoischastanet.com/), isdaT Graphic Design Department teacher in typography and typedesign, design and project coordination.

[Tanguy Vanlaeys](https://vnls-tanguy.tumblr.com/), research on CNC type started at [ANRT](https://anrt-nancy.fr/), advices on Inkscape + Hershey font usages and open paths SVG fonts export tricks.

[Frederik Berlaen](https://typemytype.com/), *otf-svgMaker* Python script for [Robofont](https://robofont.com/) exporting from any skeletal UFO source an OTF-SVF color font permitting editable open contours typographic layouts in the Adobe CC environment (CC 2019 and above). 

