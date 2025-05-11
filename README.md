# Home Brew Landing Page - Maintenance Guide

This guide will help you maintain and customize the Home Brew landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this line and change "HomeBrewCo":
```html
<a href="/" class="text-2xl font-bold text-gray-800">HomeBrewCo</a>
```

2. **Navigation Items**: Find the navigation div:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <!-- Add or modify navigation items here -->
</div>
```

### Hero Section
To update the main headline and subtext:

1. **Main Headline**: Find this section:
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">Best Home Brew Kits: Brew Your First Craft Beer at Home-No Experience Required</h1>
```

2. **Background Image**: Update the hero image URL:
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" alt="Craft Beer Brewing" class="w-full h-full object-cover">
```

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-sm`, `text-xl`, `text-2xl`, `text-4xl`
- Spacing: `px-4`, `py-2`, `mb-6`, `mt-12`
- Colors: `text-gray-600`, `bg-blue-600`, `text-white`
- Responsive design: `md:text-6xl`, `md:grid-cols-2`

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-600">

<!-- Modified for larger, darker text -->
<p class="text-2xl text-gray-800">
```

## Managing Links

### Navigation Links
Current navigation links are:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="https://briansavic.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">Shop Now</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with your new URL
3. For internal links, use `#section-id`
4. For external links, use full URLs starting with `https://`

### Call-to-Action Buttons
Update all "Shop Now" buttons:

1. Find all instances of:
```html
<a href="https://briansavic.com" class="inline-block bg-blue-600...">
```

2. Replace `https://briansavic.com` with your shop's URL

## Adding Policy Pages

### Footer Policy Links
Locate the footer policy section:

```html
<div>
    <h4 class="text-xl font-bold mb-4">Policies</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400">Terms of Service</a></li>
    </ul>
</div>
```

To add policy pages:

1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400">Terms of Service</a></li>
```

3. Ensure consistent styling by copying the header and footer from `index.html`

## Troubleshooting

### Common Issues

1. **Broken Images**
   - Check image URLs are correct
   - Verify image files exist in the specified location
   - Ensure proper image format (jpg, png, etc.)

2. **Responsive Design Problems**
   - Look for `md:` prefixed classes
   - Test on different screen sizes
   - Verify mobile menu functionality

3. **Link Issues**
   - Check for typos in URLs
   - Verify file paths for internal links
   - Test all links after updating

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes, and test thoroughly after updates.