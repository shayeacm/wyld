# Wyld Growth Website

A professional one-page website for Wyld Growth grant writing and career navigation services.

## Features

- One-page scrolling design
- Responsive layout
- Contact form with email integration
- Smooth scrolling navigation
- Nature-inspired aesthetic with brand colors
- Sections: Hero, Grants, Career, Our Approach, Testimonials, Contact

## Setup Instructions

### 1. Contact Form Setup

The contact form uses [Formspree](https://formspree.io/) to send emails to writing@griffix.ca.

**To activate the contact form:**

1. Go to [https://formspree.io/](https://formspree.io/)
2. Create a free account (if you don't have one)
3. Create a new form
4. Copy your form endpoint URL (it will look like: `https://formspree.io/f/YOUR_FORM_ID`)
5. Open `index.html`
6. Find line with: `<form class="contact-form" id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID"`
7. Replace `YOUR_FORM_ID` with your actual Formspree form ID
8. In your Formspree dashboard, set the email address to: writing@griffix.ca

### 2. Logo Images

The website currently uses a placeholder SVG logo. To use your actual logo:

1. Save your logo files to `assets/images/`
2. Update the logo path in `index.html` (line ~27):
   ```html
   <img src="assets/images/YOUR-LOGO-FILENAME.png" alt="Wyld Growth Logo" class="hero-logo">
   ```

### 3. Deployment to GitHub Pages

1. Commit all files to your repository:
   ```bash
   git add .
   git commit -m "Initial website build"
   git push origin claude/build-business-website-xHTKf
   ```

2. Go to your GitHub repository settings
3. Navigate to "Pages" in the left sidebar
4. Under "Source", select your branch (claude/build-business-website-xHTKf)
5. Click "Save"
6. Your site will be published at: `https://yourusername.github.io/wyld/`

## Customization

### Colors

Brand colors are defined in `css/styles.css` as CSS variables:

```css
:root {
    --wine: #722A3B;
    --persian-green: #1B998B;
    --teal: #327174;
    --coral: #EF767A;
    --gray: #524E58;
    --cream: #F5F1E8;
}
```

You can adjust these to match your exact brand colors.

### Content

All content is placeholder text. To update:

1. Open `index.html`
2. Find the section you want to edit
3. Replace the placeholder text with your actual content

### Fonts

The site currently uses Georgia (serif). To change fonts:

1. Add your font (Google Fonts, etc.) to the `<head>` in `index.html`
2. Update the `font-family` in `css/styles.css`

## File Structure

```
wyld/
├── index.html           # Main HTML file
├── css/
│   └── styles.css       # All styles
├── js/
│   └── script.js        # Interactive features
├── assets/
│   └── images/
│       └── wyld-growth-logo.svg
└── README.md            # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

© 2026 Wyld Growth. All rights reserved.