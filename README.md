Carthage
========

Presently this git is a placeholder, major work will not start until later this
year.

The plan is to create three OpenType fonts:

Carthage Alte:
: A font including glyphs for many of the archaic alphabetical languages around
  the Eastern part of the Mediterranean Sea from Libya, Egypt, Canaan, Anatolia,
  and further east through Mesopotamia. Mostly scripts that were in use from
  Proto-Sinaitic through Coptic. For languages like Greek and Samaritan and
  Hebrew that are still in use today, the letter forms will be closer to the
  older letter forms than to modern when there is a difference.

Carthage Veraltete:
: A font for cuneiform codepoints. As these are not an alphabetic script, they
  really should be in a distinct font file.

Carthage Neue:
: This will cover Arabic and only Arabic. Arabic is complex enough of a script
  that I believe it belongs in its own font. This font will likely have to have
  the glyphs drawn by someone very familiar with Arabic.

I will *not* create a font for Egyptian (or other) Hieroglyphs. Way too much
work.


The Point
---------

The point is to allow someone writing a paper on these ancient cultures to be
able to transcribe words and phrases from the alphabets of these cultures and
have things like the stroke width be consistent between the different scripts
used by these cultures.

The LaTeX class will just be called ‘Carthage’ and will just set up easy access
to the scripts. For example, `\carthage[phoenician]{}` will set up the argument
to use the `Carthage Alte` font using right to left writing direction, and
`\carthage[greek]{}` will do the same but left to right.

For some of the scripts, the bold variant may not contain glyphs and for some of
the scripts (most of them) the italic variant may not contain glyphs, so the
LaTeX package will actually set up proper fontspec parameters for the script
to accommodate.

Also, the LaTeX package will allow the user to choose their own preferred font
if the user does not like the glyphs provided by the fonts I will attempt to
create. In such cases, the user will have to do the fontspec parameters before
loading the LaTeX class so they can feed their fontspec name as a parameter for
the script when loading the LaTeX class. It is critical to allow users to define
their own preferred font because I have seen cases where a professor *requires*
a specific typeface for Polytonic Greek or Biblical Hebrew, etc.


Bézier Curves
-------------

These fonts will use Cubic Bézier curves. I know many operating systems prefer
quadratic for display fonts, but I really do not like them. Someone who wants
to use the fonts where Quadratic Bézier curves work better is free to convert
the fonts to use Quadratic curves themselves. 

LaTeX works fine when cubic Bézier curves are used for the glyphs, and so does
any PDF renderer.


Italic Script Variant
---------------------

When an Italic script is provided, the glyphs will be drawn closer to what a
scribe working with pen and ink would write, which is often different than what
a scribe etching the script into a hard surface would write.


LaTeX `emph{}`
--------------

LaTeX by default uses the Italic script variant when the `\emph{}` command is
used, but with these scripts it is *probably* more appropriate to use the Bold
variant by default. However, the `\emph{}` command can not just be redefined
because the author of a paper is likely writing the paper in whatever their
modern language is (e.g. English or Modern Greek or Klingon) so `\emph{}` should
not be globally redefined.

I am not yet sure how I will approach the issue. I may do nothing and just warn
the user not to use `\emph{}` and `\strong{}` in the context of the scripts
provided.


Keyboard Layouts
----------------

Keyboard Layouts that work with GNU/Linux will be provided when possible so
that direct Unicode input is easier when working in GNU/Linux.

For example, with Greek I am not happy with the existing ‘Polytonic Greek’
keyboard layout and I already know how I would improve it. As far as I know,
there is no existing keyboard layout for Phoenician or Imperial Arabic but
it would be pretty easy to make them based upon the existing Hebrew keyboard
layout. The user would not have to use them but for those who want them, I want
them available as part of this project.


Initial Glyphs
--------------

When I start this project, I will start with Greek and Phoenician. I do not yet
know where I will go from there.




