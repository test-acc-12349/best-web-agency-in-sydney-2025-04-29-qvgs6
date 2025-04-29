# WebAgency Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the WebAgency landing page. Follow these steps carefully to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">WebAgency</a>
```
Replace "WebAgency" with your company name.

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Grow your business with clicks
</p>
```

### Modifying Tailwind Classes
Common classes and their purposes:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-xl` (applies at medium screens)

Example of changing text size and color:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">Easy to Use</h3>

<!-- Modified -->
<h3 class="text-2xl font-semibold mb-4 text-blue-700">Easy to Use</h3>
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page sections):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   ```html
   <a href="#new-section-id">New Section</a>
   ```

2. External links:
   - Replace the placeholder URL:
   ```html
   <!-- Original -->
   <a href="https://fixrr.online">Get Started</a>
   
   <!-- Modified -->
   <a href="https://your-domain.com">Get Started</a>
   ```

### Call-to-Action Buttons
Update all CTA button links:
```html
<!-- Find these throughout the page -->
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600...">
```
Replace `https://fixrr.online` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Links Setup
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy and terms pages (privacy.html, terms.html)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

For links to external policy pages:
```html
<li><a href="https://your-domain.com/privacy" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Example: `href="#features"` must match `id="features"`
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the mobile-first approach intact
   - Test all changes on different screen sizes

3. **Text Styling Problems**
   - Maintain the font hierarchy:
     - Headings: `text-4xl` to `text-6xl`
     - Body text: `text-base` to `text-xl`
   - Keep consistent color schemes using Tailwind's color classes

### Need Help?
- Double-check all changes in a development environment before pushing live
- Use browser developer tools to inspect elements
- Maintain backups of the original code
- Test all links before deployment

Remember to always validate your HTML after making changes and test the page across different browsers and devices.