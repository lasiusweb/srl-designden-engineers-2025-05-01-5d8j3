# SRL Designden Landing Page Maintenance Guide

This guide will help you maintain and customize the SRL Designden landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Company Name and Logo
The company name appears in two locations:
1. Header (Navigation):
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    SRL Designden
</div>
```
2. Footer:
```html
<h3 class="text-xl font-bold mb-4">SRL Designden Engineers</h3>
```

To update, simply replace the text while keeping the surrounding HTML tags intact.

### Hero Section Text
Located near the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    Leading Engineering Consultancy Services in Process Industry
</h1>
<p class="text-xl text-gray-600 mb-12">
    Excellence in engineering solutions, from concept to completion
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main heading
2. Replace the text between the `<p>` tags for the subheading
3. Keep all class attributes unchanged to maintain styling

### Service Cards
Each service card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 border border-gray-100">
    <div class="text-blue-600 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Basic & Detailed Engineering</h3>
    <p class="text-gray-600">Comprehensive engineering solutions...</p>
</div>
```

To update:
1. Locate the service card you want to modify
2. Change the `<h3>` text for the service title
3. Update the `<p>` text for the service description
4. The SVG icon can be replaced with a different icon from [Heroicons](https://heroicons.com)

## Managing Navigation Links

### Main Navigation Menu
Located in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#about" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">About</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Update the `href` attribute:
   - For same-page sections, use `#section-id`
   - For other pages, use the full path (e.g., `/about.html`)
3. Update the link text between the `<a>` tags

### Email Links
The page contains email links in multiple locations:
```html
<a href="mailto:designden1973@gmail.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full...">
```

To update:
1. Find all instances of `mailto:designden1973@gmail.com`
2. Replace with your new email address
3. Keep the `mailto:` prefix

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout After Text Updates**
   - Verify all HTML tags are properly closed
   - Check that you haven't accidentally removed any class attributes
   - Ensure long text doesn't overflow containers

2. **Links Not Working**
   - Confirm file names match exactly (case-sensitive)
   - Verify all files are in the correct directory
   - Check that section IDs match the href attributes

3. **Responsive Design Issues**
   - Keep the responsive class prefixes intact:
     - `md:` for medium screens
     - `lg:` for large screens
   - Don't remove the `container` class from main sections
   - Maintain the existing grid structure in service cards

### Need Help?
If you encounter issues:
1. Compare your changes with the original code
2. Verify all Tailwind CSS classes remain unchanged
3. Check the browser's developer tools (F12) for errors
4. Ensure all files are saved and properly linked

Remember to test the page across different screen sizes after making changes to ensure responsive design remains intact.