# Times-Armenian-to-Unicode

A mapping table to convert **RTF** files containing text in the font **Times Armenian** to proper Armenian **Unicode**.

**Times Armenian** is a legacy font in which the [Armenian characters](https://en.wikipedia.org/wiki/Armenian_alphabet) are in the hexadecimal range **A3** to **FD**.

A special keyboard would normally have been used to type Armenian text with this obsolete [encoding](https://en.wikipedia.org/wiki/ArmSCII).

Such a legacy font is unsuitable for wider purposes in the modern world which now uses Unicode for most applications.

There exists a requirement therefore to convert text from Times Armenian to Unicode.

There are many applications that can save files as or export files to RTF.

**QuarkXPress**™ can export content in **Rich Text Format**, though the export may be lossy in respect of margin notes, etc.

**Microsoft Word**™ can save files in **Rich Text Format**, but the conversion is simpler *after* the following preprocessing step.

The RTF files to be converted should first be opened with **MS Wordpad**™ and resaved. The resulting files are much smaller.

Such an RTF file can be opened for inspection using a text editor such as **Notepad++**.

The mapping table conversion treats the RTF files as *plain text* input.

i.e. The internal RTF codes are replaced by different RTF codes that correspond to those in the Unicode block for Armenian.

The mapping table is a **tab delimited** text file with two columns.

In the **find** column, the codes are *hexadecimal*. In the **replace** column, the codes are *decimal*.

The conversion also requires the *specified* legacy font to be *replaced* by a Unicode font that supports Armenian.

The **Sylfaen** font that's installed with Windows is a suitable candidate, except for one character (see below).

The character mapping table can be called as as an external replace list in a bespoke **TextPipe** filter.

My **TextPipe** filter also replaces the font specified in the RTF header lines.

The mapping table was *reverse engineered* during April 2013. For traceability I have also uploaded my Excel workbook.

**Acknowledgement**: The excellent Unicode text editor for Windows called [BabelPad](http://www.babelstone.co.uk/Software/BabelPad.html) was invaluable in preparing this file.

The Excel worksheets are protected but without a password, merely to prevent inadvertent changes.

NB. Times Armenian does not have a character for the **Armenian Hyphen**. It had the RTF code **\\--** in its place.

FIO. It used the **small tilde \x{02DC}** in its place in some separately generated PDF files.

Both these pecularities may have been due to a quirk of how **QuarkXPress**™ exports to RTF or prints to PDF.

This exception is not currently included in my mapping table. It was rectified separately afterwards.

Likewise, the table excludes five Armenian ligatures and two other Armenian Unicode characters.

Even so, these are listed in my Excel worksheet for the sake of completeness.

The Armenian script requires a suitable Unicode font. 

NB. The **Sylfaen** font displays the Armenian Hyphen as a space. The **DejaVu Sans** font is preferred on this score.

In modern Armenian orthography, the character **և** is no longer a typographical ligature, but a distinct letter with a place in the new alphabetic sequence, before "o".

Aside: Misunderstandings may arise due to the fact the the **Unicode name** for the character **U+0587** is still ARMENIAN SMALL LIGATURE ECH YIWN. I guess this is historic, and unlikely to be changed in the near future.



