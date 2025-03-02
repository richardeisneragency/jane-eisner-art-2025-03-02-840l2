# Jane Eisner Art - Landing Page Maintenance Guide

This guide will help you maintain and customize the Jane Eisner Art landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and brand name. To update:

1. **Brand Name:**
```html
<!-- Located at the top of the page -->
<a href="/" class="font-['Playfair_Display'] text-2xl font-bold">
    Jane Eisner Art  <!-- Edit this text -->
</a>
```

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#gallery">Gallery</a>  <!-- Edit text here -->
    <a href="#shop">Shop</a>
    <a href="#commission">Commission</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main welcome section includes:

1. **Main Heading:**
```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-6xl lg:text-7xl font-bold">
    Bringing Beauty to Life,<br/>One Brushstroke at a Time  <!-- Edit this text -->
</h1>
```

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-600">
    Experience the transformative power of original artwork  <!-- Edit this text -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-bold`: Makes text bold
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color

Example of modifying responsive design:
```html
<!-- Original -->
<h1 class="text-4xl md:text-6xl lg:text-7xl">

<!-- To make text smaller -->
<h1 class="text-3xl md:text-5xl lg:text-6xl">
```

## Fixing Broken Links

### Current Link Structure
The page contains these main link types:

1. **Navigation Menu Links:**
```html
<a href="#gallery">Gallery</a>
<a href="#shop">Shop</a>
<a href="#commission">Commission</a>
<a href="#contact">Contact</a>
```

2. **Call-to-Action Links:**
```html
<a href="https://janeeisnerart.com">Explore Gallery</a>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Original -->
<a href="#gallery">Gallery</a>

<!-- Updated -->
<a href="/gallery.html">Gallery</a>
```

### Internal vs External Links
- Internal links (same website): Use relative paths
  ```html
  <a href="/gallery.html">Gallery</a>
  ```
- External links (different website): Use full URLs
  ```html
  <a href="https://example.com">External Link</a>
  ```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h4 class="font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#gallery" class="text-gray-600 hover:text-gray-900">Gallery</a></li>
        <li><a href="#shop" class="text-gray-600 hover:text-gray-900">Shop</a></li>
        <li><a href="#commission" class="text-gray-600 hover:text-gray-900">Commission</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

### Alternative Footer Layout
For a separate legal links section:

```html
<div class="mt-12 pt-8 border-t border-gray-200 text-center text-gray-500 text-sm">
    <p>&copy; 2024 Jane Eisner Art. All rights reserved.</p>
    <!-- Add this new div -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-gray-900">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-gray-900">Terms of Service</a>
    </div>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Text Not Updating:**
   - Ensure you're editing the correct section
   - Check for nested elements
   - Look for duplicate text instances

2. **Links Not Working:**
   - Verify file paths are correct
   - Ensure files exist in the specified location
   - Check for typos in href attributes

3. **Styling Issues:**
   - Confirm Tailwind CSS is properly loaded
   - Check for conflicting classes
   - Verify responsive design classes are in correct order

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12)
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code

Remember to always backup your files before making changes!