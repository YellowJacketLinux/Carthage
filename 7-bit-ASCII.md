7-bit ASCII
===========

Every font file __MUST__ have full 7-bit ASCII coverage.

The 7-bit ASCII codepoints (U+0020--U+007E) will use the ‘Classic Latin’
alphabet as shown at https://www.omniglot.com/writing/classicallatin.htm for the
‘Roman’ variant and the ‘Roman Cursive’ alphabet as shown at
https://www.omniglot.com/writing/romancursive.htm for the Italic variant.

In both cases, lower-case letters will be identical to upper-case letters. Also
in both cases, 7-bit ASCII codepoints not covered by those alphabets will use
glyphs that match the style, as every font needs to have full 7-bit ASCII
coverage.

Currently the plan is to target first century BCE versions of the glyphs.
