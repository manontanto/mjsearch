# mjsearch
### Search the Entries of MacJournal text for a Word.

I'm using MacJournal for a long time. From school days, it's very useful as Book Reference Card. I'm very grateful to Dan.

Of course it has search function originally, but not enough for me. So, I made this python script for my fancy full-text-search.

### Files 
**・index.mjml.gz**
[~/library/Application Support/MacJournal/*.mjdoc/index.mjml.gz]
This XML file index the each text file of topic to its information. **TITLE** and **ID** of each topic are involved. TITLE text is in **topic** tag, and **ID**, UUID for the text file, is 'id' attribute of **content** tag. 

**・Content/ID.[txt, rtf, rtfd]**
[~/library/Application Support/MacJournal/\*.mjdoc/\*]
Files located here is the text of entries. So, search a word in these files.

### Better to modify striprtf-0.0.15
1. Line# 115 'out.append(char) → out = out + char.encode(encoding, errors="ignore")'. For 'out' is Binary, here.

2. All 'decode, encode's need 'errors = "ignore"' for Japanese.
