# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
The main banner section contains your primary message:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Your financial success is our bottom line <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting services tailored to drive your business forward <!-- Update subheading -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets text size (increases with md:text-6xl on medium screens)
- `mb-8`: Adds margin bottom spacing
- `bg-gradient-to-r`: Creates right-flowing gradient
- `hidden md:flex`: Hides on mobile, shows as flex on medium screens

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a matching ID to that section: `<section id="your-section-name">`
3. Update the href to match: `<a href="#your-section-name">`

### Call-to-Action Links
Current external links need updating:
```html
<a href="https://theaccountants.com" class="inline-block bg-gradient-to-r...">
    Transform Your Finances
</a>
```

To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Test the link to ensure it works
3. Consider adding `target="_blank"` for external links

## Adding Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages
1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes to new page links:
   - `hover:text-purple-400`
   - `transition-colors`
   - `duration-300`

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   - Don't remove `container` and `mx-auto` classes

3. **Gradient Text Not Showing**
   - Ensure these classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
     ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes and test thoroughly across different devices and browsers.