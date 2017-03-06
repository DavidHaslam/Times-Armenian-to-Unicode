# Times-Armenian-to-Unicode

A mapping table to convert **RTF** files containing text in the font **Times Armenian** to proper Armenian **Unicode**.

**Times Armenian** is a legacy font in which the Armenian characters are in the hexadecimal range **A3** to **FD**.

A special keyboard would normally have been used to type Armenian text with this font.

Such a legacy font is unsuitable for wider purposes in the modern world which now uses Unicode for most applications.

There exists a requirement therefore to convert text from Times Armenian to Unicode.

There are many applications that can save files as or export files to RTF.

**Microsoft Word**™ can save files in **Rich Text Format**, but the conversion is simpler *after* the following preprocessing step.

The RTF files to be converted should first be opened with **MS Wordpad**™ and resaved. The resulting files are much smaller.

Such an RTF file can be opened for inspection using a text editor such as **Notepad++**.

The mapping table conversion treats the RTF files as *plain text* input.

i.e. The internal RTF codes are replaced by different RTF codes that correspond to those in the Unicode block for Armenian.

The conversion also requires the *specified* legacy font to be *replaced* by a Unicode font that supports Armenian.

The **Sylfaen** font is a suitable candidate.

The character mapping table can be called as as an external replace list in a bespoke **TextPipe** filter.

My **TextPipe** filter also replaces the font specified in the RTF header lines.
