# Maya Jade Notary Website

Professional one-page website for Maya Jade Notary services.

## Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Sticky Header**: Navigation stays visible while scrolling
- **Hero Section**: Eye-catching hero with professional notary imagery
- **Services Cards**: Six service offerings with pricing
- **Appointment Booking**: Direct integration with Google Calendar
- **About Section**: Professional credentials and certifications
- **Contact Form**: Client-side form validation with mailto fallback
- **Smooth Scrolling**: Enhanced user experience with smooth navigation

## File Structure

```
mayajadenotary/
├── index.html      # Main HTML file
├── styles.css      # All styling and responsive design
├── script.js       # JavaScript for interactivity
└── README.md       # This file
```

## Quick Start

1. Open `index.html` in any modern web browser to view the site locally
2. To deploy, upload all files to your web hosting service

## Customization

### Change Colors

Edit the CSS variables in `styles.css` (lines 8-18):

```css
:root {
    --primary-color: #1a4d2e;      /* Main green color */
    --secondary-color: #4f7942;    /* Secondary green */
    --accent-color: #d4af37;       /* Gold accent */
    --text-dark: #2c3e50;          /* Dark text */
    --text-light: #ffffff;         /* Light text */
}
```

### Change Hero Image

Replace the image URL in `styles.css` (line 138):

```css
background-image: url('YOUR_IMAGE_URL_HERE');
```

Or use a local image:

```css
background-image: url('images/hero.jpg');
```

### Update Contact Email

Change the email address in `script.js` (line 91) to your actual email:

```javascript
const mailtoLink = `mailto:YOUR_EMAIL@mayajadenotary.com?subject=...`;
```

### Integrate a Form Backend

To connect a real form backend (like Formspree, Netlify Forms, or a custom backend):

1. Sign up for a form service
2. Update the form submission handler in `script.js` (starting at line 78)
3. Replace the `simulateFormSubmission` function with an actual API call

Example with Formspree:

```javascript
function submitToFormspree(data) {
    fetch('https://formspree.io/f/YOUR_FORM_ID', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(data)
    })
    .then(response => response.json())
    .then(data => {
        showMessage('Thank you! I\'ll respond within one business hour.', 'success');
        contactForm.reset();
    })
    .catch(error => {
        showMessage('Sorry, there was an error. Please try again.', 'error');
    });
}
```

## Deployment Options

### Option 1: Static Hosting (Recommended)

Deploy to any of these free services:

- **Netlify**: Drag and drop the folder at netlify.com
- **Vercel**: Connect your GitHub repo at vercel.com
- **GitHub Pages**: Push to GitHub and enable Pages in settings
- **Cloudflare Pages**: Deploy via cloudflare.com

### Option 2: Traditional Web Hosting

Upload all files via FTP/SFTP to your web hosting provider's `public_html` or `www` directory.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Accessibility Features

- Semantic HTML5 elements
- ARIA labels for interactive elements
- Keyboard navigation support
- Reduced motion support for users with motion sensitivity
- High contrast text for readability

## Performance

- Minimal dependencies (no frameworks)
- Fast loading time
- Optimized CSS and JavaScript
- Mobile-first responsive design

## Contact Form Notes

The current form uses a `mailto:` fallback, which opens the user's email client. For a better user experience, consider integrating with:

- **Formspree** (free tier available): formspree.io
- **Netlify Forms** (if hosting on Netlify)
- **EmailJS** (client-side email service)
- **Your own backend API**

## License

© 2025 Maya Jade Notary. All rights reserved.

## Support

For questions or customization help, contact the developer or refer to standard HTML/CSS/JavaScript documentation.
