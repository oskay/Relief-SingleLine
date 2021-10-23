# Relief Single Line

*Relief SingleLine* is the single line companion of [Relief](https://github.com/isdat-type/relief) oriented towards CNC and fablabs environment.

## Existing CNC mill & laser typographic tools
Nowadays there is still a critically small amount of “central-line” or “single-stroke” fonts optimized for fablab environments and CNC mill or laser engraving practices, allowing the use of letters based on a single central line. Simultaneously, typographic tools dedicated to CNC engraving (such as [Hershey Text](https://wiki.evilmadscientist.com/Hershey_Text) extension on Inkscape) are hard to use, limited and the drawing quality of the proposed fonts doesn’t match current typographic standards. The existing offer (both commercial and open source) of single stroke fonts is very basic and the majority of these available typefaces are qualitatively deceptive (irregular drawing quality, poor spacing, no kerning, etc.). With the recent variable fonts technology, the typedesign field is currently in a boom, but strangely the rapidly democratizing domain of fablabs is hardly approached by typedesigners. This potential space for experimentation is practically left to engineers and “makers” which, despite all their noticeable efforts, need more typographic expertise and the help of the typedesign community.

## Relief, a skeletal font for fablabs and CNC engravings
Relief is a versatile sans serif “central-line” typeface with open contours and skeletal letters designed for “makers” and fablabs’ environments by students of the Graphic Design Department of the Institut Supérieur des Arts et du Design de Toulouse / [isdaT](https://www.isdat.fr/) (Élisa Garzelli & Noëlie Dayma), a project proposed by François Chastanet (isdaT Graphic Design Department teacher) part of *Les Communs / Bibliothèque Infinie* pedagogical program curated by Nathalie Bruyère (isdaT Design Department teacher). The structure of this alphabet is influenced by Adrian Frutiger’s little known and underrated Vectora typeface. The idea is having things working honestly with as less kerning as possible, a sturdy design more based on drawing solutions than infinite kerning pairs. Relief comprises an additional ornamental geometric set matching with both uppercases and lowercases’ heights. 

Relief allows the user to drastically reduce the engraving / cutting machines’ runtime while offering a quality Bézier curves rendering. Relief project is based on a main skeletal .glyphs source and explores different font format exports: [Relief](https://github.com/isdat-type/reief) with classic closed outlines for print and web on one side (OTF, TTF, WOFF), *Relief SingleLine* as a skeleton font for engraving on the other side (open path OTF-SVG for Adobe, UFO for Fontlab Pad or Drawbot, SVG for Inkscape + Hershey Text Module and closed TTF for CAD softwares). 

When using *Relief SingleLine* font for laser or mill applications, it is recommended to use the *cutting* function at low intensity and not the *engraving* function in order to reduce inscription’s tracing time on any surface (do preliminary laser power tests to determine the best speed / power couple for each material to engrave with an inscription).


## How to use it?

### OpenType-SVG color font method
As this project is primarily focusing on graphic user interface solutions opened the largest possible audiences, the Relief CNC typeface is distributed as an OpenType-SVG color font format in order to simplify the layout process for the 2D fablab community, i.e. having a central-line font editable in popular vector graphics and typographic softwares such as Illustrator or Indesign. OpenType-SVG technology represents an interesting alternative to permit single-stroke fonts wider distribution and easier use. To our knowledge, Relief CNC is the first real skeletal font working in the Adobe CC environment (CC 2019 and above), opening new perspectives for the makers worldwide. Fablab users oriented towards 2D graphic practices can now easily access quality Bézier curves and kerning in their central-line typographical layouts!

Simply install the “Relief SingleLine-Regular_svg.otf” on your system and open Illustrator or Indesign, compose your paragraphs and titlings; when the layout is finished, just use the /Text/Vectorize function (shift+command+O) to obtain a skeletal design to export as PDF or SVG file to engrave through your prefered CNC machine (laser or mill).

*Relief SingleLine* export as OpenType-SVG format was made possible thanks to [Frederik Berlaen](https://typemytype.com/)’s *otf-svgMaker* Python script for [Robofont](https://robofont.com/). This script permits to export any skeletal UFO-based font project towards and OTF-SVG font.

→fonts/otf-svg/
→scripts/Robofont_otf-svgMaker/

### UFO / FontLab Pad or Drawbot method
UFO format ([Unified Font Objects](https://unifiedfontobject.org/)) is a cross-platform, cross-application, human readable format for storing font data. Download the Relief UFO file, open it with [FontLab Pad](https://www.fontlab.com/fontlab-pad/) text editor (free of use, available for Windows and Mac), type your text, then export it as an PDF or SVG composition that you can open in any vector graphics software, run CNC. The UFO file can also be used in [Drawbot](https://www.drawbot.com/) to export towards PDF or SVG textual vector patterns to engrave. 

→fonts/ufo/

### OTF + Inkscape Hershey Text extension SVG fonts method

First install Relief-Regular.otf on your system, then parallelly copy Relief-Regular.svg there: (macOS) Applications/Inkscape (show package content) / Contents / Resources / share / inkscape / extensions / svg_fonts / Relief-Regular.svg. Compose your layout in [Inkscape](https://inkscape.org/) using Relief-Regular.otf, launch [Hershey Text extension](https://www.evilmadscientist.com/2019/hershey-text-v30/) (now available by default) to render your text blocks as skeletal letters: go to Extension / Text / Hershey Text, in font select *Other* (bottom of the list after the existing Hershey fonts) and type Relief-Regular in the next field of the dialog box as a path/name, then apply rendering. Beware to first copy your source text blocks: after the Hershey Text extension rendering process, texts are becoming not editable. Contrary to the Fontlab Pad method, Hershey Text extension unfortunately apparently disables the kerning values even if truly embedded in the SVG font.

→fonts/svg/

Process to export towards (old) SVG format with open contours (thanks to Tanguy Vanleys):

• Open UFO file in Fontforge, export as SVG,

• Open the SVG file in a text editor (such as Sublime Text) and run two find & replace actions:

— find z" /
— replace by " /

— find zM
— replace by M.


### Closed TTF for CAD softwares method 
[Rhinoceros 3D](https://www.rhino3d.com/) and some other CAD softwares are able to use closed TTF single stroke fonts by opening the closed contours the right way in its design interface with various views. When operating the text tools dialog box you have a special feature to tick to permit single stroke fonts usage (Windows version only); select the desired TTF. But composing paragraphs is simply impossible, it is limited to write some words on the same basline (no line breaks possible apparently), so quite limited to basic titling only.

→fonts/ttf-closed

## Typographic engraving proofs

First laser engraving tests on plywood at various speeds and laser powers, [Artilect](https://artilect.fr/) fablab, Toulouse, 2021 / 03 / 23.

![](https://github.com/isdat-type/Relief-SingleLine/blob/main/documentation/images/photos/relief_laser_2021_03_25_a.jpg)
![](https://github.com/isdat-type/Relief-SingleLine/blob/main/documentation/images/photos/relief_laser_2021_03_25_b.jpg)

## Contributors

Élisa Garzelli & Noëlie Dayma, isdaT Graphic Design Department students.

[François Chastanet](http://francoischastanet.com/), isdaT Graphic Design Department teacher in typography and typedesign, design and project coordination.

[Tanguy Vanleys](https://vnls-tanguy.tumblr.com/), research on CNC type started at [ANRT](https://anrt-nancy.fr/), advices on Inkscape + Hershey font usages and open contours SVG fonts export tricks.

[Frederik Berlaen](https://typemytype.com/), *otf-svgMaker* Python script for [Robofont](https://robofont.com/) exporting from any skeletal UFO source an OTF-SVF color font permitting editable open contours typographic layouts in the Adobe CC environment (CC 2019 and above). 

