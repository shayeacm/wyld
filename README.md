# Wyld Growth Website

A professional one-page website for Wyld Growth grant writing and career navigation services.

## Features

- One-page scrolling design with smooth navigation
- Fully responsive layout (desktop, tablet, mobile)
- Contact form with email integration
- Nature-inspired aesthetic with custom brand colors
- Sections: Hero, Grants, Career, Our Approach, Testimonials, Contact
- Interactive animations and hover effects

## Setup Instructions

### 1. Contact Form Setup

The contact form uses [Formspree](https://formspree.io/) to send emails to writing@griffix.ca.

**To activate the contact form:**

1. Go to [https://formspree.io/](https://formspree.io/)
2. Create a free account
3. Create a new form
4. Copy your form endpoint URL (it will look like: `https://formspree.io/f/xyzabc123`)
5. Open `index.html`
6. Find line 214 with: `<form class="contact-form" id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID"`
7. Replace `YOUR_FORM_ID` with your actual Formspree form ID
8. In your Formspree dashboard, the submissions will automatically go to the email associated with your account
9. Optionally, configure Formspree to forward to writing@griffix.ca

### 2. Logo Customization (Optional)

The website currently uses a placeholder SVG logo with botanical elements. To use your own logo:

1. Save your logo file to `assets/images/` (supported formats: PNG, JPG, SVG)
2. Open `index.html`
3. Find line 27: `<img src="assets/images/wyld-growth-logo.svg" alt="Wyld Growth Logo" class="hero-logo">`
4. Replace the filename with your logo filename

### 3. Local Preview

To view the website on your local machine:

**Option A: Direct Open (Simple)**
```bash
# Navigate to the project directory
cd /path/to/wyld

# Open index.html in your default browser
# On Mac:
open index.html

# On Windows:
start index.html

# On Linux:
xdg-open index.html
```

**Option B: Local Server (Recommended for development)**
```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Then open browser to:
# http://localhost:8000
```

### 4. Deployment to GitHub Pages

**Step 1: Push to GitHub**
```bash
# Make sure you're on the correct branch
git status

# Add all files
git add .

# Commit changes
git commit -m "Initial Wyld Growth website"

# Push to your branch
git push -u origin claude/fix-code-execution-error-GXk4T
```

**Step 2: Merge to main branch (if desired)**
```bash
# Switch to main branch
git checkout main

# Merge your feature branch
git merge claude/fix-code-execution-error-GXk4T

# Push to main
git push origin main
```

**Step 3: Enable GitHub Pages**
1. Go to your repository on GitHub: https://github.com/shayeacm/wyld
2. Click "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select the branch you want to publish (usually `main`)
5. Select folder: `/ (root)`
6. Click "Save"
7. Wait a few minutes for GitHub to build and deploy
8. Your site will be live at: `https://shayeacm.github.io/wyld/`

## Customization Guide

### Updating Colors

Brand colors are defined in `css/styles.css` at the top:

```css
:root {
    --wine: #722A3B;           /* Deep wine/burgundy */
    --persian-green: #1B998B;  /* Teal/green */
    --teal: #327174;           /* Darker teal */
    --coral: #EF767A;          /* Light coral/pink */
    --gray: #524E58;           /* Dark gray for text */
    --cream: #F5F1E8;          /* Cream background */
}
```

Simply change the hex codes to your preferred colors.

### Updating Content

All content is in `index.html`. Key sections to customize:

- **Line 38-42**: Hero tagline and description
- **Line 53-76**: Grant Writing services
- **Line 83-106**: Career Navigation services
- **Line 113-136**: Our Approach philosophy
- **Line 143-179**: Client testimonials (replace with real ones)
- **Line 214-241**: Contact form fields

### Changing Fonts

To use different fonts:

1. Add font import to `<head>` in `index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Your+Font&display=swap" rel="stylesheet">
```

2. Update font-family in `css/styles.css`:
```css
body {
    font-family: 'Your Font', serif;
}
```

### Adding More Sections

To add a new section:

1. Add section to HTML before the footer
2. Add navigation link in the navbar
3. Style in CSS following existing patterns

## File Structure

```
wyld/
├── index.html              # Main HTML file
├── css/
│   └── styles.css          # All styles and responsive design
├── js/
│   └── script.js           # Interactive features & smooth scrolling
├── assets/
│   └── images/
│       └── wyld-growth-logo.svg  # Placeholder logo
└── README.md               # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Tech Stack

- **HTML5**: Semantic structure
- **CSS3**: Custom styling with CSS variables, flexbox, grid
- **Vanilla JavaScript**: No dependencies, lightweight interactions
- **Formspree**: Form submission handling

## Next Steps

1. ✅ Preview the site locally
2. ⚙️ Set up Formspree for contact form
3. 🎨 Customize content with your actual text
4. 🖼️ Replace logo with your brand files
5. 🚀 Deploy to GitHub Pages
6. 📧 Test contact form
7. 📱 Test on mobile devices

## License

© 2026 Wyld Growth. All rights reserved.