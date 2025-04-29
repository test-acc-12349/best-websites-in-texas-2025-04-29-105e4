# Texas Web Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```
- Replace "Texas Web" with your desired company name
- The `text-blue-600` class controls the blue color
- `text-2xl` controls the size

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Replace text between `>` and `</a>` for each menu item
- Keep the `href` attributes matching your section IDs
- The `hidden md:flex` ensures mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In Texas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- Update heading and subheading text as needed
- Maintain the responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)
- The `mb-6` and `mb-12` classes control spacing

### Tailwind CSS Class Guide
Common classes used throughout:
- Size classes: `text-xl`, `text-2xl`, etc.
- Colors: `text-blue-600`, `text-gray-900`, etc.
- Spacing: `px-6`, `py-4`, `mb-12`, etc.
- Responsive prefixes: `md:`, `lg:`

## Managing Links

### Navigation Links
Current navigation links include:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The site contains several external links:
```html
<a href="https://sigmaseo.io" class="inline-flex items-center...">
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link after updating
3. Consider adding `target="_blank"` for external links

### Footer Links
Located in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Blog</a></li>
    <!-- Additional links -->
</ul>
```
- Replace `#` with actual page URLs
- Update link text as needed
- Maintain the hover effects and spacing classes

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the Legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling

Example structure for policy pages:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout:**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes use correct breakpoint prefixes

2. **Links Not Working:**
   - Verify file paths are correct
   - Check that section IDs match href attributes
   - Ensure files are in the correct directory

3. **Styling Issues:**
   - Confirm Tailwind CSS CDN is loading
   - Check for conflicting classes
   - Verify proper nesting of elements

For additional help:
- Reference [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test on multiple devices and browsers

Remember to always test changes in a development environment before pushing to production.