# Perth Luxury Tiles Landing Page - Maintenance Guide

This guide will help you maintain and customize the Perth Luxury Tiles landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

```html
<!-- Location: Line 19 -->
<a href="/" class="text-2xl font-bold text-gray-800">Perth Luxury Tiles</a>
```

To change the company name, simply replace "Perth Luxury Tiles" with your desired text.

#### Navigation Menu Classes
The navigation menu uses these key Tailwind classes:
- `space-x-8`: Creates horizontal spacing between menu items
- `text-gray-600`: Sets default text color
- `hover:text-gray-900`: Darkens text on hover

Example of modifying menu item spacing:
```html
<!-- Change space-x-8 to space-x-4 for less spacing -->
<div class="hidden md:flex space-x-4">
```

### Hero Section
The hero section contains your main headline and call-to-action button.

To update the main headline:
```html
<!-- Location: Lines 38-40 -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Luxury Floor Tiles in Perth – Transform Your Space Today
</h1>
```

The headline uses responsive text sizes:
- `text-4xl`: Default size
- `md:text-5xl`: Medium screens
- `lg:text-6xl`: Large screens

### Features and Benefits Sections
Each feature card uses consistent styling:
```html
<div class="bg-gray-50 rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
```

To modify card appearance:
- Change background: Replace `bg-gray-50` with colors like `bg-white` or `bg-gray-100`
- Adjust padding: Modify `p-8` to `p-6` or `p-10`
- Change shadow: Use `shadow-md` for lighter or `shadow-2xl` for stronger shadow

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal sections, keep the `#` prefix followed by the section's ID
2. For external links, use the full URL:
```html
<a href="https://example.com/features">Features</a>
```

### Social Media Links
Located in the footer:
```html
<!-- Location: Footer section -->
<a href="#" class="hover:text-white transition-colors duration-300">
    <i class="fab fa-facebook"></i>
</a>
```

Replace `#` with your actual social media URLs:
```html
<a href="https://facebook.com/yourbusiness" class="hover:text-white transition-colors duration-300">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:

```html
<!-- Location: Footer Quick Links section -->
<div>
    <h4 class="text-white text-lg font-bold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#features" class="hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - If elements overlap on mobile, check for proper responsive classes
   - Ensure `md:` prefixes are used for medium screen adaptations

2. **Missing Icons**
   - If Font Awesome icons don't appear, verify the CDN link is working:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
   ```

3. **Incorrect Spacing**
   - Use Tailwind's spacing utilities:
     - `p-{number}` for padding
     - `m-{number}` for margin
     - `space-x-{number}` for horizontal spacing
     - `space-y-{number}` for vertical spacing

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links point to valid URLs
- Ensure all IDs referenced in navigation match section IDs in the HTML

Remember to test all changes across different screen sizes using your browser's developer tools before deploying to production.