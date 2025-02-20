# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Logo
</div>

<!-- Replace "Logo" with your company name -->
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight">
    Lorem ipsum dolor
</h1>
<!-- Replace with your main headline -->

<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Lorem ipsum dolor
</p>
<!-- Replace with your subheading -->
```

### Tailwind CSS Class Modifications

Common classes and their purposes:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-{weight}`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-{size}`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-{size}`: Adds padding top and bottom
- `px-{size}`: Adds padding left and right

To modify responsive design:
```html
<!-- Example of responsive classes -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- Explanation:
- text-4xl: Default size on mobile
- md:text-5xl: Medium screens (768px+)
- lg:text-6xl: Large screens (1024px+)
-->
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal section links, keep the `#` prefix
2. Ensure the ID matches your section:
```html
<!-- Section ID must match the href -->
<section id="features" class="py-24 bg-white">
```

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Blog</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Careers</a></li>
</ul>
```

To update:
1. Replace `#` with your actual URL
2. For external links, use complete URLs:
```html
<a href="https://yourwebsite.com/about">About</a>
```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to your footer section:
```html
<!-- Find the footer columns -->
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Add a new column or update existing -->
    <div>
        <h3 class="text-xl font-bold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Maintaining Consistent Styling
Copy these classes for new links:
```html
class="text-gray-400 hover:text-white transition duration-300"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that section IDs match href attributes exactly
   - Check for extra spaces in IDs
   - Ensure sections have unique IDs

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify breakpoint classes (md:, lg:) are correctly ordered
   - Test all screen sizes

3. **Missing Styles**
   - Confirm Tailwind CSS CDN link is working
   - Check for typos in class names
   - Ensure classes are properly spaced

For additional help:
- Use browser developer tools (F12) to inspect elements
- Reference [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)