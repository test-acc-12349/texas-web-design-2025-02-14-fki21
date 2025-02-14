# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections to Update

#### Header (Logo and Navigation)
```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>

<!-- Navigation Items -->
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- More navigation items -->
</div>
```
To update:
- Change "TWD" to your desired logo text
- Modify navigation items by editing the text between `<a>` tags

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
To update:
- Replace heading text between `<h1>` tags
- Update subheading text between `<p>` tags
- Maintain responsive text sizes (don't remove `md:` or `lg:` prefixes)

### Understanding Tailwind Classes

Key class prefixes:
- `text-`: Controls text size and color
- `bg-`: Sets background color
- `p-`: Controls padding
- `m-`: Controls margin
- `md:`: Applies styles on medium screens and up
- `lg:`: Applies styles on large screens and up

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="px-8 py-4 bg-blue-600 text-white rounded-full">

<!-- Modified for green color -->
<a href="#" class="px-8 py-4 bg-green-600 text-white rounded-full">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="...">Get Started</a>
```

### Updating Links
1. Internal Links (sections on same page):
   - Keep the `#` symbol
   - Match the ID of the target section
   - Example: `<a href="#features">` links to `<section id="features">`

2. External Links:
   - Replace `https://twd.com` with your actual website URL
   - Example:
   ```html
   <!-- Before -->
   <a href="https://twd.com">Get Started</a>
   
   <!-- After -->
   <a href="https://yourwebsite.com">Get Started</a>
   ```

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-sm">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<ul class="space-y-2 text-sm">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
- Don't remove responsive prefixes (`md:`, `lg:`)
- Keep the original structure of utility classes
- Test on different screen sizes

3. Missing Styles
- Verify the Tailwind CDN link is working
- Check for typos in class names
- Maintain spaces between multiple classes

### Getting Help
- Refer to [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the browser's developer tools (F12) for errors
- Verify all files are in the correct directory structure

Remember to:
- Always test changes across different devices and browsers
- Keep a backup of the original files before making changes
- Maintain consistent styling throughout the page
- Test all links after updating them

Need more help? Contact your web development team or refer to the Tailwind CSS documentation for detailed guidance on specific classes and utilities.