This folder is your portfolio, exported for the web.

  index.html  the page itself: your projects, in 3D, with your write-ups
  data.json   everything the page reads
  models/     a copy of each project's model
  thumbs/     a copy of each project's thumbnail

TO PUT IT ONLINE

  1. Make a new repository on GitHub.
  2. Upload everything in this folder to it.
  3. In the repository, open Settings, then Pages, and set the source
     to your main branch.
  4. GitHub gives you a URL. That is the link you share.

Nothing here needs a server of your own - it is all static files.

TO LOOK AT IT ON THIS COMPUTER FIRST

Double-clicking index.html will not work. A browser will not let a page
opened straight off disk read the files next to it, so the page would
have nothing to show. Serve the folder instead: open a terminal here and
run

  python -m http.server 8000

then open http://localhost:8000 in your browser. (The page says this too
if you forget.)

A NOTE ON PART ORDER

Your notes, joints and animations point at parts by position. data.json
carries the part names in the order this app loaded them, and the viewer
matches on those names rather than trusting that a browser walks your
model the same way. Renaming parts in CAD after writing notes about them
is the one thing that will move a note onto the wrong part.
