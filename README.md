serialize-functions
===================

**Functions for clean or serialize string.**

1. Remove accents
-----------------

Replace all accented characters by same characters non-accented.

    $example = 'ÀÆÕùî';
    $clean = $this->removeAccent($example);
    echo $clean; /* AAEOui */

Replaced characters : 

    À Á Â Ã Ä Å Æ à á â ã ä å æ
    Ç ç
    È É Ê Ë è é ê ë
    Ì Í Î Ï ì í î ï
    Ñ ñ
    Ò Ó Ô Õ Ö Œ ò ó ô õ ö œ
    Ù Ú Û Ü ù ú û ü
    Š š
    Ý Ÿ ý ÿ
    Ž ž
    Ø ø ß Ð ƒ ?

2. Remove non-filename characters
---------------------------------

Replace all non-filename characters by "-".

    $example = "This*is|a<simple>example";
    $clean = $this->removeNonFilenameCaract($example);
    echo $clean; /* This-is-a-simple-example */

Replaced characters : `*  |  \  /  .  :  ;  "  <  >  ?`

3. No whitespaces
-----------------

Replace all whitespaces by "-".

    $example = "This is a simple example";
    $clean = $this->noWhitespace($example);
    echo $clean; /* This-is-a-simple-example */

4. No whitespaces at all
------------------------

Remove all whitespaces.

    $example = "This is a simple example";
    $clean = $this->removeNonFilenameCaract($example);
    echo $clean; /* Thisisasimpleexample */

