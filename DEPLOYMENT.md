# Waslet Landing Page - Deployment Guide

## Quick Start

The landing page is ready to deploy! You can view it locally by opening `index.html` in any web browser, or by running a local server:

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if you have npx)
npx serve .

# PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Pre-Deployment Checklist

### 1. Replace Placeholder Assets
- [ ] Update `assets/waslet-logo.svg` with your actual logo
- [ ] Replace `assets/hero-phone-mockup.svg` with real app mockup
- [ ] Add actual app screenshots to replace `app-screenshot-*.svg`
- [ ] Update `assets/waslet-og-image.svg` for social media sharing

### 2. Update App Store Links
- [ ] Replace the Google Play Store URL in `index.html`:
  ```html
  href="https://play.google.com/store/apps/details?id=com.waslet.app"
  ```
  Change `com.waslet.app` to your actual app package name.

### 3. Configure Form Handling

#### Option A: Formspree (Recommended)
1. Sign up at [Formspree.io](https://formspree.io)
2. Create two forms: one for business signups, one for newsletter
3. Replace the form actions:
   ```html
   <!-- Business form -->
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   
   <!-- Newsletter form -->
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

#### Option B: Google Forms
1. Create Google Forms for business and newsletter signups
2. Update form actions to point to your Google Form URLs

#### Option C: Custom Backend
Replace form actions with your API endpoints.

### 4. Update Contact Information
- [ ] Update email addresses in form actions (`business@waslet.com`, `updates@waslet.com`)
- [ ] Add your actual contact information
- [ ] Update footer links to point to real pages

### 5. Add Analytics (Optional)
Add your tracking code before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 6. SEO Optimization
- [ ] Update Open Graph URL with your actual domain
- [ ] Add structured data markup (optional)
- [ ] Submit sitemap to Google Search Console

## Deployment Options

### Option 1: Static Hosting (Recommended)

#### Netlify
1. Drag and drop the entire folder to [Netlify Drop](https://app.netlify.com/drop)
2. Or connect your Git repository for automatic deployments

#### Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project directory
3. Follow the prompts

#### GitHub Pages
1. Push code to GitHub repository
2. Enable GitHub Pages in repository settings
3. Select source branch (main/master)

#### AWS S3 + CloudFront
1. Create S3 bucket with static website hosting
2. Upload files to bucket
3. Configure CloudFront for CDN (optional)

### Option 2: Traditional Web Hosting
Upload all files via FTP/SFTP to your web hosting provider's public folder.

### Option 3: Self-Hosted
Deploy on your own server using Apache, Nginx, or any web server.

## Post-Deployment Tasks

### 1. Test All Functionality
- [ ] Test on mobile, tablet, and desktop
- [ ] Verify all links work
- [ ] Test form submissions
- [ ] Check loading speed
- [ ] Validate HTML/CSS

### 2. Monitor Performance
- [ ] Set up analytics tracking
- [ ] Monitor Core Web Vitals
- [ ] Track conversion rates
- [ ] Monitor form submissions

### 3. SEO Setup
- [ ] Submit to Google Search Console
- [ ] Create and submit XML sitemap
- [ ] Set up Google My Business (if applicable)
- [ ] Monitor search rankings

## UTM Parameters for Tracking

Add UTM parameters to your Play Store links for better tracking:

```
https://play.google.com/store/apps/details?id=com.waslet.app&utm_source=website&utm_medium=cta&utm_campaign=landing_page
```

## Security Considerations

- All external links use `rel="noopener noreferrer"`
- Forms use `mailto:` fallbacks (no server-side vulnerabilities)
- No JavaScript means no XSS attack vectors
- Static files only (no server-side code)

## Maintenance

### Regular Updates
- Update app screenshots when UI changes
- Refresh testimonials periodically
- Update store/merchant count numbers
- Keep Google Play badge current

### Content Updates
All content can be easily updated by editing `index.html`. The responsive design will automatically adapt to content changes.

## Support

For technical issues with the landing page, refer to:
- Browser developer tools for debugging
- W3C HTML/CSS validators
- Lighthouse for performance auditing
- WAVE for accessibility testing

## File Structure Summary
```
waslet-landing/
├── index.html                 # Main page
├── styles.css                 # All styling
├── README.md                  # Project documentation
├── DEPLOYMENT.md              # This file
├── validation-checklist.md    # PRD compliance check
└── assets/
    ├── waslet-logo.svg
    ├── hero-phone-mockup.svg
    ├── app-screenshot-1.svg
    ├── app-screenshot-2.svg
    ├── app-screenshot-3.svg
    ├── app-screenshot-4.svg
    ├── google-play-badge.png
    ├── favicon.svg
    └── waslet-og-image.svg
```

The landing page is production-ready and follows all PRD specifications!