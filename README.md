# BuySell Marketplace Website

A modern, responsive, and clean website for a buying and selling marketplace platform. Built with HTML, CSS, and JavaScript.

## Features

- **Hero Section** - Eye-catching hero section with call-to-action buttons
- **About Section** - Detailed information about the platform with feature highlights
- **Services Section** - Four service cards showcasing platform features
- **Testimonials Section** - User reviews and ratings
- **Contact Form** - Functional contact form with validation
- **Responsive Design** - Fully responsive for mobile, tablet, and desktop
- **Smooth Animations** - Subtle animations and transitions throughout
- **Modern UI** - Clean, minimal design with a professional look

## Color Scheme

**Professional Marketplace Theme** - Optimized for buying/selling platforms:

- **Primary Color**: `#00b894` (Teal/Turquoise) - Trust, Growth, Modern, Money
- **Primary Dark**: `#00a085` (Darker Teal)
- **Primary Light**: `#55efc4` (Light Teal)
- **Secondary Color**: `#2c3e50` (Deep Navy) - Professional, Trustworthy
- **Accent Color**: `#f39c12` (Orange) - Energy, Call-to-Action, Urgency
- **Success Color**: `#27ae60` (Green) - Positive actions, Money
- **Background**: White with light gray sections

## File Structure

```
├── index.html      # Main HTML file
├── style.css       # All CSS styles
├── script.js       # JavaScript functionality
└── README.md       # This file
```

## Customization Guide

### Changing Colors

To change the color scheme, edit the CSS variables in `style.css`:

```css
:root {
    --primary-color: #00b894;  /* Teal - Trust, Growth, Modern */
    --primary-dark: #00a085;   /* Darker teal */
    --primary-light: #55efc4;  /* Lighter teal */
    --secondary-color: #2c3e50; /* Deep Navy - Professional */
    --accent-color: #f39c12;   /* Orange - Energy, CTAs */
    --success-color: #27ae60;  /* Green - Success, Money */
}
```

The current theme uses a **Professional Marketplace** color scheme optimized for e-commerce and buying/selling platforms. The teal primary color conveys trust and growth, while the orange accent creates energy for call-to-action buttons.

### Updating Content

1. **Hero Section**: Edit the hero section in `index.html` (lines ~45-60)
2. **About Section**: Modify the about content in `index.html` (lines ~64-95)
3. **Services**: Update service cards in `index.html` (lines ~98-150)
4. **Testimonials**: Edit testimonial cards in `index.html` (lines ~153-210)
5. **Contact Info**: Update contact information in `index.html` (lines ~213-230)

### Adding Images

Replace placeholder images from Unsplash with your own:

1. **Hero Background**: Line ~43 in `index.html`
   ```html
   background-image: url('your-image-url.jpg');
   ```

2. **About Image**: Line ~90 in `index.html`
   ```html
   <img src="your-image-url.jpg" alt="Description">
   ```

3. **Testimonial Images**: Lines ~165, ~177, ~189, ~201 in `index.html`
   ```html
   <img src="your-image-url.jpg" alt="Name">
   ```

### Modifying Fonts

The website uses Google Fonts (Poppins). To change the font:

1. Update the Google Fonts link in `index.html` (line ~12)
2. Change the `--font-primary` variable in `style.css` (line ~34)

### Form Submission

The contact form currently uses a simulated submission. To connect it to a backend:

1. Edit the form submission handler in `script.js` (lines ~100-130)
2. Replace the setTimeout simulation with an actual API call:

```javascript
fetch('your-api-endpoint', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        name,
        email,
        phone,
        subject,
        message
    })
})
.then(response => response.json())
.then(data => {
    showFormMessage('Thank you! Your message has been sent.', 'success');
    contactForm.reset();
})
.catch(error => {
    showFormMessage('Error sending message. Please try again.', 'error');
});
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Dependencies

- **Font Awesome 6.4.0** - For icons (loaded via CDN)
- **Google Fonts (Poppins)** - For typography (loaded via CDN)

No build process or package installation required!

## Usage

1. Download all files to your project directory
2. Open `index.html` in a web browser
3. That's it! No installation needed.

## Customization Tips

### Adding New Sections

1. Add HTML structure in `index.html`
2. Add corresponding styles in `style.css`
3. Update navigation if needed
4. Add scroll animations in `script.js` if desired

### Modifying Animations

Animations are controlled in `script.js` (Intersection Observer section). To adjust:

- Change `threshold` value for when animations trigger
- Modify `rootMargin` for offset timing
- Adjust CSS transition durations in `style.css`

### Responsive Breakpoints

Current breakpoints:
- **Desktop**: 969px and above
- **Tablet**: 768px - 968px
- **Mobile**: 480px - 767px
- **Small Mobile**: Below 480px

Modify these in the `@media` queries in `style.css`.

## License

This project is open source and available for personal and commercial use.

## Support

For questions or issues, please contact: support@buysell.com

---

**Note**: Replace placeholder content, images, and contact information with your actual details before deploying.

