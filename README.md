# Landing Page Maintenance Guide

This guide will help you maintain and customize the SparkyAI landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<a href="#" class="text-xl font-semibold">SparkyAI</a>
```
Simply replace "SparkyAI" with your brand name.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Features</a>
```
- Change the text between `>` and `</a>` to update menu items
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Automate Your Recruiting, Grow Your Team, <span class="text-gray-500">Without Chasing Anyone!</span>
</h1>
```

To modify:
- Update the text between the `<h1>` tags
- The `<span>` tag creates the gray-colored text
- Don't remove the responsive classes (`text-4xl md:text-5xl lg:text-6xl`)

### Understanding Tailwind Classes

Key classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `font-bold`: Bold text weight
- `text-gray-900`: Dark gray text color
- `mb-8`: Bottom margin spacing

## Managing Links

### Current Link Locations

1. **Navigation Menu:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="https://phghub.ai/funnel-welcome-home.php?id=mtg">Get Started</a>
</div>
```

2. **Call-to-Action Buttons:**
```html
<a href="https://phghub.ai/funnel-welcome-home.php?id=mtg" class="inline-flex items-center justify-center px-8 py-4 border border-transparent rounded-lg">
    Start Automating Now
</a>
```

3. **Footer Email:**
```html
<a href="mailto:sparkyai@gmail.com">sparkyai@gmail.com</a>
```

### Updating Links

To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. For internal links (same page sections):
   - Use `#section-id` format
   - Example: `href="#features"`
4. For external links:
   - Use complete URLs starting with `https://`
   - Example: `href="https://your-domain.com/page"`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert these lines in the footer section before the copyright notice:

```html
<div class="flex space-x-6">
    <a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Privacy Policy</a>
    <a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Terms of Service</a>
</div>
```

### Step 2: Update Footer Grid
Modify the footer grid to accommodate new links:

```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-center">
    <div>
        <p class="text-gray-600">Contact us at: <a href="mailto:sparkyai@gmail.com" class="text-gray-900 hover:text-gray-700">sparkyai@gmail.com</a></p>
    </div>
    <div class="text-center">
        <div class="flex justify-center space-x-6">
            <a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Privacy Policy</a>
            <a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Terms of Service</a>
        </div>
    </div>
    <div class="text-right">
        <p class="text-gray-600">&copy; 2024 SparkyAI. All rights reserved.</p>
    </div>
</div>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout:**
   - Check that all opening tags have matching closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure the Tailwind CDN link is present in the head section

2. **Links Not Working:**
   - Verify file names match exactly (case-sensitive)
   - Check that files are in the correct directory
   - Ensure external URLs include `https://`

3. **Responsive Issues:**
   - Keep the `md:` and `lg:` prefixed classes for responsive design
   - Test the page at different screen sizes
   - Don't remove the viewport meta tag in the head section

Remember:
- Always backup your files before making changes
- Test all links after updating
- View your page in multiple browsers
- Check mobile responsiveness using browser dev tools

Need more help? Contact technical support or consult the Tailwind CSS documentation for detailed class references.