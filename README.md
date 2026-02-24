# Performance Paddle Camp — Website

Static HTML website for Performance Paddle Camp. Hosted on GitHub Pages.

## Pages

| File | Page | Purpose |
|------|------|---------|
| `index.html` | Home | Primary landing page, two CTAs |
| `camp.html` | The Camp | System explanation, format, levels |
| `sessions.html` | Nantucket Sessions | Schedule + inquiry form |
| `club.html` | Your Club | Club visit service + inquiry form |
| `coaches.html` | Coaches | Mike, Ana, staff bios |
| `nantucket.html` | Nantucket Experience | Destination selling, travel info |
| `results.html` | Results | Testimonials and success stories |
| `faq.html` | FAQ | Accordion-style Q&A |
| `contact.html` | Contact | General contact form |
| `thank-you.html` | Thank You | Post-submission confirmation |

## Setup

### 1. GitHub Pages Hosting

1. Create a new GitHub repository (e.g., `performancepaddlecamp.github.io` for a user site, or any name for a project site)
2. Push all files to the `main` branch
3. Go to **Settings → Pages → Source** → select `main` branch, root folder
4. Site will be live at `https://yourusername.github.io/repo-name/`

### 2. Custom Domain (Optional)

1. Buy a domain (e.g., `performancepaddlecamp.com`)
2. In your DNS provider, add a CNAME record pointing to `yourusername.github.io`
3. In the GitHub repo, go to **Settings → Pages → Custom domain** → enter your domain
4. Check "Enforce HTTPS"

### 3. Forms (Formspree)

Forms currently point to placeholder Formspree endpoints. To activate:

1. Create a free account at [formspree.io](https://formspree.io)
2. Create 3 forms:
   - **Nantucket Session Inquiry** → get form ID
   - **Club Visit Inquiry** → get form ID  
   - **General Contact** → get form ID
3. Replace these placeholders in the HTML files:
   - `sessions.html` → replace `YOUR_FORMSPREE_ID`
   - `club.html` → replace `YOUR_FORMSPREE_ID_CLUB`
   - `contact.html` → replace `YOUR_FORMSPREE_ID_CONTACT`
4. In each Formspree form settings, set the redirect URL to `thank-you.html`

Free tier: 50 submissions/month (more than enough for 32 bookings/year + club inquiries).

### 4. Images

The site currently uses Unsplash placeholder images. Replace with actual camp photography:

- Hero backgrounds: 1600px wide minimum, landscape orientation
- Coach headshots: Square, at minimum 400×400px
- Replace the `coach__photo--placeholder` divs with actual `<img>` tags

Recommended: Create an `images/` folder and host images locally in the repo.

## Updating Content

### Session Availability Badges
In `index.html` and `sessions.html`, update the badge classes:
- `badge--open` → "Courts Available" (green)
- `badge--limited` → "Limited" (amber)
- `badge--sold-out` → "Sold Out" (red)

### Adding Testimonials
Copy an existing `.testimonial` block in `results.html` and update the text, author, and role.

### Updating Dates
Search and replace dates across files when rolling to a new season:
- `September 9 – 11` through `September 15 – 17`
- `September 2025`
- `2025` in footers and content

## Tech Stack

- Pure HTML/CSS/JS — no build step, no dependencies
- Google Fonts: DM Serif Display + Source Sans 3
- CSS custom properties for theming
- Intersection Observer for scroll animations
- Formspree for form handling (free tier)
- GitHub Pages for hosting (free)

**Total monthly cost: $0** (or ~$12/year for a custom domain)
