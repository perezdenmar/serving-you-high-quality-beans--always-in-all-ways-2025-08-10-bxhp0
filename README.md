# Coffa Landing Page - Maintenance Guide

This guide will help you maintain and customize the Coffa coffee landing page. It's written for beginners who are new to HTML and CSS.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold">Coffa</a>
```
Simply replace "Coffa" with your desired brand name.

2. **Announcement Bar:**
```html
<div class="bg-black text-white text-center py-2 text-sm">
    <p>Free Shipping on Orders Over $50</p>
</div>
```
Modify the text between `<p>` tags to change the announcement message.

### Hero Section
The main banner section contains your primary messaging:

```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">Serving you high-quality beans. Always in all ways</h1>
    <p class="text-xl md:text-2xl mb-8">Premium Beans, Perfectly Roasted—Crafted for Every Cup.</p>
</div>
```

To modify:
- Change the h1 text to update your main headline
- Update the p tag content for your subheading
- The `md:text-6xl` means text size will be larger on medium screens and up
- `mb-6` adds margin bottom spacing (can be adjusted from 1-16)

### Tailwind CSS Class Guide
Common classes used throughout:
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `font-{weight}`: Controls text thickness (normal, medium, bold, etc.)
- `bg-{color}`: Sets background color (white, black, gray-50, etc.)
- `p-{number}`: Adds padding (1-16)
- `m-{number}`: Adds margin (1-16)
- `rounded-{size}`: Adds border radius (sm, md, lg, full)

## Managing Links

### Navigation Menu Links
Current placeholder links in the navigation:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Shop</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">About</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Contact</a>
</div>
```

To update links:
1. Replace `#` with your actual URL
2. Example: `<a href="about.html">` for internal pages
3. Example: `<a href="https://yourstore.com/shop">` for external links

### Call-to-Action (CTA) Links
The main "Buy Now" button appears multiple times:
```html
<a href="https://tinyurl.com/coffaceph" class="inline-block bg-white text-black px-8 py-4 rounded-full">Shop Now</a>
```

Update all instances of `https://tinyurl.com/coffaceph` to your actual store URL.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add privacy/terms links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
        <!-- Existing items -->
        <li>Fast Worldwide Shipping (5 days delivery)</li>
        <li>100% Satisfaction Guarantee</li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common Issues:
1. **Broken Links**: Check for typos in URLs and ensure files exist in the correct directory
2. **Responsive Issues**: 
   - Always test both mobile (`sm:`) and desktop (`md:`) classes
   - Use browser dev tools to test different screen sizes
3. **Style Changes Not Working**:
   - Verify Tailwind CSS is properly loaded
   - Check for typos in class names
   - Classes are case-sensitive

Need Help?
- Use browser inspection tools (F12) to examine elements
- Refer to [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test all changes across different devices and browsers

Remember to always backup your files before making significant changes.