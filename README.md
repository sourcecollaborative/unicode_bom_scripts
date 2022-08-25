# unicode_bom_scripts
This project contains a few useful unicode processing scripts: addbom and removebom.

ADDBOM: This script adds the Unicode Byte Order Mark (BOM) to the beginning of
a file. This is rarely needed. However there is one exception: Microsoft Excel
quite idiotically will not tree a file as UTF-8 unless a BOM is present. It would
be better if Excel simply checked whether a file contained UTF-8 characters. Such
a check is rather trivial to perform. But alas, it is Microsoft ...

REMOVEBOM: This script removes a Unicode Byte Order Mark (BOM) from the beginning
of a file, if one is present. This too is rarely needed, as in general BOMs are
not used very much. However, some Unicode-agnostic software may try to display or
print the BOM which, depending on your use case, may be detrimental. So here we
have `removebom` which performs the complement operation to `addbom`.


