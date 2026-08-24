# Course data

The three course files are generated locally by `scripts/build-data.py`.

- `daily.json`: everyday English vocabulary
- `ielts.json`: IELTS and academic English vocabulary
- `business.json`: professional and business English vocabulary
- `manifest.json`: counts, difficulty distribution, and available topics

Each record includes the answer, part of speech, difficulty, topic, definition,
complete sentence, Chinese translation, blanked sentence, hint, and source type. Source definitions
and source example sentences come from Princeton WordNet via NLTK. Frequency
ranking comes from the `wordfreq` package. Generated definition sentences are
used only when WordNet has no suitable example containing the exact answer.

Run `python scripts/build-data.py` to rebuild and validate all data files.
Run `python scripts/add-translations.py` after rebuilding to restore the local
Chinese translations and remove first-letter hints.
