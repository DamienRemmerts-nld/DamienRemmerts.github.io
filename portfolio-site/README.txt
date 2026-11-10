HOW TO ADD YOUR PHOTOS
======================

Folder layout (keep it exactly like this):

  index.html      <- the website
  photos.json     <- the list of your photos
  images/         <- put your photo files here

1. Prepare your photos
   Save them as JPEG, about 1600 px on the long edge, ideally under 500 KB each.
   Use simple file names with no odd characters, e.g. milky-way.jpg

2. Copy the files into the images/ folder.

3. Add one block per photo to photos.json:

   {
     "file": "milky-way.jpg",        <- exact file name in images/
     "title": "Milky Way over the ridge",
     "category": "Night sky",        <- becomes a filter button
     "info": "14mm · f/2.8 · 20s",   <- optional, shown when opened
     "cs": 2,                        <- optional: tile is 2 columns wide
     "rs": 2                         <- optional: tile is 2 rows tall
   }

   - Put a comma between blocks, but NOT after the last one.
   - Leave out cs/rs for a normal small tile. Use them for your best shots.
   - Delete the three example blocks that don't match your files.

4. Upload the whole folder to GitHub Pages / Netlify / your server.

TO TEST ON YOUR COMPUTER
Opening index.html by double-clicking won't load photos.json (browsers block it).
Either test on GitHub Pages, or run a tiny local server from the folder:
  python3 -m http.server
then open http://localhost:8000

Everything else (your name, bio, skills, projects) is edited in index.html:
search for the comments that say EDIT.
