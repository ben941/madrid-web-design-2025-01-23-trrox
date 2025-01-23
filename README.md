# Madrid Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Madrid Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold text-blue-600">MWD</a>
```
- Replace "MWD" with your desired logo text
- The `text-blue-600` class controls the blue color

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Servicios</a>
    <!-- Additional menu items -->
</div>
```
- Replace "Servicios" with your desired menu text
- Keep the `href` attributes matching your section IDs

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Web Design In Madrid
</h1>
```
- Update the heading text while maintaining the classes
- The classes control responsive text sizes:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Tailwind CSS Class Guide
Common classes used throughout:
- `container mx-auto`: Centers content
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-600`: Sets text color
- `bg-white`: Sets background color
- `rounded-2xl`: Adds rounded corners
- `shadow-lg`: Adds box shadow

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Servicios</a>
<a href="#benefits">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contacto</a>
```
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Update the displayed text

### External Links
Current external links:
```html
<a href="https://mwd.com" class="inline-block bg-blue-600">
```
To update:
1. Replace `https://mwd.com` with your actual website URL
2. Test the link to ensure it works
3. Keep the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacidad</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Términos</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacidad</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Términos</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Ensure section IDs match exactly with href attributes
- Check for typos in IDs
- IDs are case-sensitive

2. **Responsive Design Issues**
- Check that you've maintained responsive classes (md: and lg: prefixes)
- Test on different screen sizes
- Don't remove container classes

3. **Styling Problems**
- Keep the Tailwind CSS link in the head section
- Maintain the class structure when updating
- Don't remove transition classes for hover effects

4. **External Links Not Working**
- Verify URLs include https:// or http://
- Test links in a new tab
- Ensure no spaces in URLs

Remember:
- Always make backups before changes
- Test all changes on multiple browsers
- Keep the responsive design intact
- Maintain consistent styling across sections

Need help? Contact support at admin@mwd.com or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).