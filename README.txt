INTERIM LOADING SCREEN
======================
Files: index.html, background.jpg and the folder sounds (with bed.ogg inside). Put them ALL in the same place online (keep the sounds folder as a folder), then tell the server where.

PUTTING IT ON GITHUB PAGES (free)
1. Make a free account at github.com (if you do not have one).
2. Click the + at the top right, then "New repository". Name it anything (for example "interim-loading"). Choose Public. Click "Create repository".
3. On the new repository page click "uploading an existing file". Drag in index.html, background.jpg and the whole sounds folder (or make the folder on GitHub with "Add file", "Create new file", typing sounds/ before a name, and upload bed.ogg into it), then click "Commit changes".
4. Click "Settings" (top of the repository), then "Pages" (left side).
5. Under "Build and deployment", set Source to "Deploy from a branch", Branch to "main" and the folder to "/ (root)", then Save.
6. After a minute or two the page shows your address at the top, like:  https://YOURNAME.github.io/interim-loading/
   Open it in a browser to check you see the smoke picture fading in.

TELLING THE SERVER
In the server's server.cfg add this line (with YOUR address, keep the quotes):
   sv_loadingurl "https://YOURNAME.github.io/interim-loading/"
Restart the server. Players now see it while they connect.

CHANGING IT LATER
Edit the numbers at the top of index.html (marked EDIT) or swap background.jpg for another picture with the same name, and upload again.

SOUND
The quiet bed (sounds/bed.ogg) repeats while the page is open. Settings are at the top of the script in index.html:
  BED_VOLUME 0.5 (lower = quieter), BED_FADE_IN 4 seconds, BED_FADE_OUT 2.5 seconds.
In a normal web browser the sound waits for a click; inside the game it starts on its own.
