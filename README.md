# Fitform Landing Page Maintenance Guide

This guide will help you maintain and customize the Fitform landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">Fitform</a>
```
Replace "Fitform" with your desired company name.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900">Kenmerken</a>
```
- Replace "Kenmerken" with your desired menu text
- Keep the `href="#features"` if linking to a section on the same page
- Update both desktop AND mobile menu items

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Sta Op Stoel Fitform
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Tijdelijk 10% Korting op het Gehele Assortiment
</p>
```

To modify:
1. Update the h1 text between the tags
2. Adjust text size using Tailwind classes:
   - `text-4xl`: Default size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Tailwind CSS Tips for Beginners
- Classes starting with `md:` apply to medium screens and up
- Classes starting with `lg:` apply to large screens and up
- Color classes follow the pattern: `text-{color}-{shade}`
- Spacing classes use the format: `m-{size}` for margin, `p-{size}` for padding

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center...">
```

### Updating Links
1. **Internal Links** (same page sections):
   ```html
   <!-- Original -->
   <a href="#features">Kenmerken</a>
   
   <!-- Updated Example -->
   <a href="#new-section">New Section</a>
   ```
   Make sure the href matches the `id` of the target section.

2. **External Links** (other websites):
   ```html
   <!-- Original -->
   <a href="https://sta-opstoelen.nl">
   
   <!-- Updated Example -->
   <a href="https://your-website.com">
   ```
   Always include the full URL with `https://`

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer section:
```html
<div>
    <h3 class="text-lg font-bold mb-4">Juridisch</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
```

### Maintaining Consistent Styling
Copy these classes for new links to match existing styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section `id` attributes match the href values
   - Ensure no spaces in IDs
   - IDs should be unique

2. **Responsive Design Issues**
   - Check mobile menu functionality
   - Verify media query classes (md:, lg:) are correct
   - Test on different screen sizes

3. **Style Inconsistencies**
   - Copy existing Tailwind classes for similar elements
   - Maintain color scheme using provided color classes
   - Keep spacing consistent using similar margin/padding values

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates to your live site.