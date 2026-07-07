KADENWITTIG.COM — SITE FILES
=============================

STRUCTURE
---------
index.html              → Home / work grid
reels.html              → All four reels
about.html              → Bio and credits
contact.html            → Contact page
project-template.html   → Duplicate this for each project page
css/style.css           → All styles
images/                 → Put your thumbnail and hero images here

TO CUSTOMIZE
------------
1. IMAGES
   - Add thumbnail images to the /images/ folder
   - In index.html, replace each <div class="thumb-placeholder"> with:
     <img src="images/your-image.jpg" alt="Project Name" />
   - Recommended thumbnail size: 1920x1080px (16:9)
   - Headshot for about page: any portrait ratio, 1200px wide minimum

2. REELS
   - Upload reels to Vimeo
   - In reels.html, replace the Vimeo video IDs (the number in the iframe src)
   - Format: https://player.vimeo.com/video/YOUR_VIDEO_ID

3. PROJECT PAGES
   - Duplicate project-template.html for each project
   - Name them: project-from-a-distance.html, project-pillar.html, etc.
   - Update the <title>, hero image, meta fields, description, and video embed
   - In index.html, each work-item already links to the right filename

4. FONTS
   - Loaded from Google Fonts (requires internet connection)
   - Cormorant Garamond (headings) + Montserrat (labels/nav)

DEPLOYING TO GITHUB PAGES
--------------------------
1. Create a free account at github.com
2. Create a new repository named: kadenwittig.com (or any name)
3. Upload all these files to the repository
4. Go to Settings → Pages → Source: main branch / root folder
5. GitHub will give you a .github.io URL

CONNECTING YOUR NAMECHEAP DOMAIN
----------------------------------
1. In your GitHub repo, create a file named: CNAME
   Contents of the file (one line): kadenwittig.com

2. In Namecheap dashboard → Domain List → kadenwittig.com → Manage → Advanced DNS:
   Delete existing A records, then add:

   Type: A Record    Host: @    Value: 185.199.108.153
   Type: A Record    Host: @    Value: 185.199.109.153
   Type: A Record    Host: @    Value: 185.199.110.153
   Type: A Record    Host: @    Value: 185.199.111.153
   Type: CNAME       Host: www  Value: YOUR-GITHUB-USERNAME.github.io.

3. Wait 30–60 minutes for DNS to propagate
4. In GitHub Pages settings, enter your custom domain and enable HTTPS
