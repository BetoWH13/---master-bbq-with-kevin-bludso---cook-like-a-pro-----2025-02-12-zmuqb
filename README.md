# BBQ Masters Landing Page - Maintenance Guide

This guide will help you maintain and customize the BBQ Masters landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line in the header:
```html
<div class="text-2xl font-bold text-gray-800">BBQ Masters</div>
```
Simply replace "BBQ Masters" with your desired text.

2. **Navigation Menu Items**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
The main banner section contains:

1. **Main Heading**: Update this text:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight">
    🔥 Master BBQ with Kevin Bludso & Cook Like a Pro! 🍖
</h1>
```

2. **Subheading**: Modify this line:
```html
<p class="text-xl md:text-2xl text-gray-600 leading-relaxed">
    Learn BBQ from Kevin Bludso & Master Grilling Skills!
</p>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-{color}-{shade}` (e.g., `text-gray-600`)
- Responsive classes start with screen sizes: `md:` or `lg:`
- Spacing uses format `p-{number}` for padding, `m-{number}` for margin

## Managing Links

### Navigation Links
Current internal links are:
- `#features`
- `#benefits`
- `#contact`

To update these:
1. Find the corresponding section ID in the HTML
2. Update the `href` attribute in the navigation
```html
<!-- Example: Changing Features link -->
<a href="#new-section-id" class="text-gray-600 hover:text-gray-900">New Name</a>
```

### Call-to-Action Links
The main CTA button appears multiple times. Update all instances:
```html
<a href="https://www.cookingguildclass.com/#aff=BetoWH72" class="inline-block bg-orange-600...">
```
Replace the URL with your new destination.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these placeholder links in the footer:
```html
<div class="space-y-4">
    <h3 class="text-xl font-bold text-white mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or incorrect class names
   - Verify responsive classes use correct breakpoints (`md:`, `lg:`)

3. **Images Not Loading**
   - Verify image URLs are correct
   - Check file permissions
   - Ensure image files exist at specified locations

### Need Help?
- Double-check the Tailwind CSS documentation for correct class names
- Use browser developer tools (F12) to inspect elements
- Verify all files are in the correct directory structure
- Test all links after making changes

Remember to always backup your files before making significant changes, and test the page across different devices and browsers after updates.