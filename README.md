# mjsearch
### Search the Entries of MacJournal for a Word.

### Better to modify striprtf.py
1. Line# 115 'out.appen(char) → out = out + char.encode(encoding, errors="ignore")'. For 'out' is Binary, here.
2. All 'decode, encode's need 'errors = "ignore"' for Japanese.
