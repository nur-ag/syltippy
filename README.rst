Syltippy: Spanish Word Syllabization in Python!
===============================================

Spanish is a beautiful language spoken by almost 500 million people around the world. Among its
nice features, undoubtedly put there by a very prescient designer, is the fact that its syllabic
structure is regular enough to be manageable by a computer. Since spanish is the loving 
tongue, this is helpful if you want to programmatically analyze spanish poetry or song lyrics — and
there is a lot of that, too! 

Syltippy is a simple, user friendly word syllabization package with no additional dependencies.
It is a port of the TIP Syllabizer [http://tulengua.es/en/syllabification] and the related 
paper "Automatic syllabification for Spanish using lemmatization and derivation to solve the
prefix’s prominence issue" [https://doi.org/10.1016/j.eswa.2013.06.056]. For my own convenience, I 
used the Java version, silabas4j [https://github.com/vic/silabas4j] when porting the code. 

Syltippy supports both Python 2 and 3 through a very simple interface. So simple, in fact, that it
is just one function: syllabize(word). syllabize returns a tuple <syllables, stress> that
respectively contain the list of syllables in the input word and the index of the syllable that is 
stressed within the word.

You can use Syltippy to naturally hyphenate text, analyze poetry or compute statistics about text
corpora in spanish.

Installation & Usage
--------------------

To install Syltippy, simply run:

    $ pip install syltippy

Usage is similarly simple:

    >>> from syltippy import syllabize
    >>> syllables, stress = syllabize(u'supercalifragilísticoespialidoso')
    >>> print(u'-'.join(s if stress != i else s.upper() for (i, s) in enumerate(syllables)))
    su-per-ca-li-fra-gi-lis-ti-co-es-pia-li-DO-so

As you can see, we get the syllables and stress for our not-so-long but just-so-sweet word and turn
them into a hyphenated string with the stressed syllable in all caps. 
Supercalifragilisticoespialidoso indeed!

License
-------

Syltippy is released under the same license as the original TIP syllabizer, GNU General Public 
License. 


