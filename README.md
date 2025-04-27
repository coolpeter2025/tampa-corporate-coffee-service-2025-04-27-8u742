# DelightfulBean Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DelightfulBean corporate coffee service landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-amber-500 to-orange-600 bg-clip-text text-transparent">
    DelightfulBean  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items**
```html
<!-- Both desktop and mobile menus need to be updated -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main landing section contains the primary heading and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight mb-6 bg-gradient-to-r from-amber-500 to-orange-600 bg-clip-text text-transparent">
    Tampa Corporate Coffee Service  <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Tampa's premier mobile coffee experience  <!-- Update subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-gray-100`, `text-gray-300`, `text-gray-400`
- Spacing: `px-6`, `py-4`, `mt-4`, `mb-12`
- Responsive prefixes: `md:`, `lg:` (e.g., `md:text-5xl`)

## Fixing Broken Links

### Navigation Links
1. Internal section links are prefixed with #:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. External links need full URLs:
```html
<!-- Update the booking link URL -->
<a href="https://www.delightfulbean.com/" class="inline-block px-8 py-4...">
    Book Your Experience
</a>
```

### Social Media Links
Located in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Facebook</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Instagram</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">LinkedIn</a></li>
</ul>
```
Replace `#` with actual social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Links to Footer
Insert the following code in the footer's Quick Links section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Use the same header and footer structure
3. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match href attributes
- Section IDs should be unique
- Example: `<section id="features">` matches `<a href="#features">`

2. **Responsive Design Issues**
- Check mobile view using browser dev tools
- Verify media query classes (md:, lg:) are correct
- Example: `class="text-4xl md:text-5xl lg:text-7xl"`

3. **Color Gradient Issues**
```html
<!-- Gradient text requires all these classes -->
class="bg-gradient-to-r from-amber-500 to-orange-600 bg-clip-text text-transparent"
```

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all files are in the correct directory
- Test all links after making changes
- Use browser developer tools to inspect elements

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.