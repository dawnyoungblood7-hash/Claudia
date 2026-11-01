# Build tools for index.html

These scripts produced the interactive page from the reading text.

1. `build.py`: inserts the Leningrad Codex Hebrew (Westminster Leningrad Codex 4.20,
   from the Open Scriptures Hebrew Bible, `wlc/Gen.xml`) and the English/Parallel/Hebrew
   and pointing controls (`add.css`, `add.js`).

       python3 build.py josephite_genesis_final.html Gen.xml step1.html

2. `enhance.py`: makes the sigla clickable, marks every place where whole verses were
   removed, links each omission to its Apparatus category and preface rationale, and
   embeds the omitted verses (World English Bible, current edition, from
   github.com/TehShrike/world-english-bible, plus the WLC Hebrew) (`enhance.css`, `enhance.js`).

       python3 enhance.py step1.html Gen.xml genesis.json enhance.css enhance.js index.html

`enhance.py` checks that the omitted verses match the Apparatus table exactly and stops if they do not.
