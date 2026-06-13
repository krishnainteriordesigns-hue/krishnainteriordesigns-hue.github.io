KRISHNA INTERIORS WEBSITE — README
==================================

FOLDER STRUCTURE (place all of this inside /Users/pavan/Claude/Interiors)
-------------------------------------------------------------------------
Interiors/
├── index.html              <- the website (open this in a browser)
├── update_gallery.py       <- run after adding/removing photos
├── README.txt
├── assets/
│   └── logo.png            <- PUT YOUR LOGO HERE (this name exactly)
└── gallery/
    ├── gallery.js          <- auto-generated photo list (don't edit by hand)
    └── images/
        ├── kitchens/       <- sub-folder name = category shown on site
        ├── ceilings/
        ├── glass-works/
        └── partitions/     <- add more sub-folders any time (e.g. upvc, painting)


1. CHANGE THE LOGO
------------------
Save your logo as:   assets/logo.png
Refresh the browser. Done.
(PNG with transparent background looks best, roughly square or tall.
If no logo.png exists, the site falls back to a built-in ribbon mark.)


2. ADD PHOTOS OF YOUR WORK
--------------------------
Step 1: Copy photos into gallery/images/<category>/
        - The sub-folder name becomes the filter category on the site
          (e.g. "glass-works" shows as "Glass Works").
        - The file name becomes the caption
          (e.g. "modular-kitchen-mg-road.jpg" -> "Modular Kitchen Mg Road").
        - Supported: .jpg .jpeg .png .webp .gif .svg

Step 2: Open Terminal in the Interiors folder and run:
            python3 update_gallery.py

Step 3: Refresh the website. New photos appear on the "Our Work" page
        with category filters and a full-screen lightbox.

NOTE: The 6 images currently in gallery/images/ are branded SAMPLE
placeholders so you can see how the page behaves. Delete them and
re-run update_gallery.py once you add real photos.


3. VIEWING THE SITE
-------------------
Double-clicking index.html works in most browsers. If photos ever don't
load when opened as a file, serve it locally instead:

    cd /Users/pavan/Claude/Interiors
    python3 -m http.server 8000

then open http://localhost:8000


4. PUBLISHING LATER
-------------------
The whole folder is plain static files — it can be uploaded as-is to any
host (Netlify, GitHub Pages, cPanel, etc.). Just remember to run
update_gallery.py before uploading whenever photos change.
