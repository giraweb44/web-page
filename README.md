# Waslet Landing Page

A single-page marketing website for Waslet, a delivery app for food, fresh produce, cosmetics, and general goods.

## Features

- **Mobile-first responsive design** - Works perfectly on all devices
- **Pure HTML + CSS** - No JavaScript dependencies for maximum compatibility
- **Green & white brand theme** - Professional and clean design
- **SEO optimized** - Includes meta tags and Open Graph for social sharing
- **Accessibility compliant** - WCAG AA standards with proper focus management
- **Fast loading** - Optimized assets and minimal external dependencies

## Structure

```
/
├── index.html          # Main landing page
├── styles.css          # All styling and responsive design
├── assets/             # Images and assets
│   ├── waslet-logo.svg
│   ├── hero-phone-mockup.svg
│   ├── app-screenshot-*.svg
│   ├── google-play-badge.png
│   └── favicon.svg
└── README.md           # This file
```

## Sections

1. **Header** - Navigation with logo and links
2. **Hero** - Main value proposition with Google Play download
3. **Features** - 4 key features with icons
4. **How it Works** - 3-step process explanation
5. **Screenshots** - App preview images
6. **Testimonials** - Social proof with star ratings
7. **Business Signup** - Form for merchants and drivers
8. **Newsletter** - Email capture for updates
9. **Footer** - Links and company information

## Usage

Simply open `index.html` in any modern web browser. The page is fully self-contained and doesn't require a web server for local viewing.

For production deployment:
1. Upload all files to your web server
2. Update the Google Play Store link with your actual app URL
3. Configure the form actions to point to your backend or email service
4. Add your actual app screenshots and logo
5. Update the Open Graph image URL with your domain

## Customization

### Colors
The brand colors are defined as CSS custom properties in `styles.css`:
- Primary green: `#27AE60`
- Accent green: `#A8E6CF` 
- Light green: `#B9F6CA`

### Content
All text content can be easily updated in `index.html`. The design is flexible and will adapt to content changes.

### Images
Replace the placeholder SVG files in the `/assets` folder with your actual:
- Logo (recommended size: 40x40px)
- Hero phone mockup (recommended size: 300x600px)
- App screenshots (recommended size: 200x400px each)
- Favicon (32x32px)

## Performance

- Optimized for fast loading with minimal HTTP requests
- Uses system fonts for better performance
- SVG assets for crisp display on all screen resolutions
- CSS animations with `prefers-reduced-motion` support

## Browser Support

Compatible with all modern browsers including:
- Chrome/Edge 88+
- Firefox 85+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Forms

The contact forms use `mailto:` actions as fallbacks. For production, consider:
- Formspree.io for serverless form handling
- Google Forms integration
- Custom backend API endpoints

## Analytics

To add analytics, insert your tracking code before the closing `</head>` tag in `index.html`.

## License

This landing page template is created for Waslet. Modify as needed for your specific requirements.