# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the AIBizBots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold">AIBizBots</a>

<!-- How to modify -->
<a href="/" class="text-2xl font-bold">Your Company Name</a>
```

#### Hero Section
Look for the `<h1>` and `<p>` tags within the hero section:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">
    Pickaxe, Make and Relevance AI Integrations
</h1>
<p class="text-xl md:text-2xl mb-8">
    Pickaxe, Make Scenarios and Relevance AI Agents in One Spot
</p>
```
Replace the text between these tags with your desired content.

### Understanding Tailwind Classes

Key classes explained:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens and up
- `font-bold`: Bold text weight
- `mb-6`: Margin bottom spacing
- `container`: Centers content with max-width
- `mx-auto`: Horizontal auto margins
- `px-4`: Horizontal padding
- `py-4`: Vertical padding

To modify responsive design:
```html
<!-- Original -->
<div class="text-4xl md:text-6xl">

<!-- Make text smaller -->
<div class="text-3xl md:text-5xl">

<!-- Add more responsive breakpoints -->
<div class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example:
```html
<!-- Adding a new link -->
<a href="#pricing" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Pricing</a>
```

### External Links
The main call-to-action links currently point to:
```html
<a href="https://aibizbots4u.com/store">
```

To update:
1. Replace all instances of `https://aibizbots4u.com/store` with your store URL
2. Search for this URL in the document (usually 4-5 instances)
3. Example:
```html
<a href="https://your-store-url.com/products">
```

## Linking Privacy and Terms Pages

### Footer Policy Links
Current placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Returns</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    <li><a href="returns.html" class="hover:text-white transition-colors duration-300">Returns</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Section IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` breakpoint classes are working
   - Common fix: Add `responsive` meta tag if missing:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Missing Styles**
   - Verify Tailwind CSS CDN is loading
   - Check browser console for errors
   - Ensure classes are spelled correctly

### Need Help?
- Contact email: Update in footer section
```html
<a href="mailto:your-email@domain.com">your-email@domain.com</a>
```

Remember to test all changes in multiple browsers and screen sizes before deploying to production.