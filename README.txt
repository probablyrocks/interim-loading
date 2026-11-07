INTERIM LOADING SCREEN
======================
Files: index.html (the page, with the looping smoke animation stored inside it) and the folder sounds (with bed.ogg inside).
Put both in the same place online. The picture is inside index.html on purpose: the game's own browser would not show it when it was a separate file.

PUTTING IT ON GITHUB PAGES (free)
1. Make a free account at github.com and a new Public repository (any name, for example "interim-loading").
2. On the repository page click "uploading an existing file". Drag in index.html and the sounds folder (or add the folder with "Add file", "Create new file", typing sounds/ before a name, and upload bed.ogg into it). Commit.
3. Settings, then Pages. Source "Deploy from a branch", Branch "main", folder "/ (root)", Save.
4. After a minute or two it shows your address, like https://YOURNAME.github.io/interim-loading/ . Open it in a browser to check.

TELLING THE SERVER
In the server's server.cfg add (with YOUR address, keep the quotes):
   sv_loadingurl "https://YOURNAME.github.io/interim-loading/"
Restart the server.

CHANGING IT LATER
- Animation: ask Claude to put a new one into index.html (it has to be stored inside the page; keep it a short loop).
- Darkness: the last number in #shade in index.html (0 = none).
- Sound: the settings at the top of the script in index.html: BED_VOLUME 0.5 (lower = quieter), BED_FADE_IN 4 seconds, BED_FADE_OUT 2.5 seconds.
  In a normal web browser the sound waits for a click; inside the game it starts on its own.
