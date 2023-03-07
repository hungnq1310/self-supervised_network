# self-supervised_network

## Data
Processing OpenSubtitle dataset based on opensubtitles-parser.py of Domerin: https://github.com/domerin0/opensubtitles-parser

Version: v1.
Reference: Jorg Tiedemann. 2009. News from opus-a collection of multilingual parallel corpora with tools and interfaces. In Proceedings of the 2nd Recent advances in natural language processing (RANLP), volume 5, pages 237–248.
Website: https://opus.nlpl.eu/index.php

Note!!: code of opensubtitles-parser has been changed for convenience.
Changes: 
  1. adding `.decode("utf-8")` after `.encode('ascii', 'ignore')` will avoid error: `TypeError: a bytes-like object is required, not 'str' `

  2. because `xmlFiles` variable contains 2 files: `.info` and `.xml`, which make the `tree.parser` can't get the value in `.xml` file and I don't see any mention from original opensubtitles-parser.py of Domerin. This can avoid following error `...not well-formed (invalid token): line 1, column 0`
  
### Usage
You should download the dataset from link below:
  http://opus.lingfil.uu.se/download.php?f=OpenSubtitles/en.tar.gz
Then extract in data folder. After that, run `opensubtitles-parser.py`. This will convert the XML format into format text `.txt`

Note!! (from Domerin): 
Some words are appearing in the corpus file without a space between tokens (ex/ and the -> andthe) I don't know if this is from the original dataset, or a problem with my script. I need to look more into it.

 
 
  
  
