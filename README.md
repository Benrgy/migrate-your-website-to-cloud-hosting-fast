# MigrateHost Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the MigrateHost landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-blue-600">MigrateHost</div>
```
- Replace "MigrateHost" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600)

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Keep the `hover:text-blue-600` class for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-8">
    Seamlessly Migrate Your Website to Cloud Hosting—Fast, Secure, Hassle-Free
</h1>
```
- Replace heading text while maintaining the dash (—) formatting
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)
- `mb-8` controls bottom margin (options: mb-4, mb-12, mb-16)

### Features and Benefits Sections
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Scalable Resources</h3>
    <p class="text-gray-600">Your description here</p>
</div>
```
- Update headings in `<h3>` tags
- Modify descriptions in `<p>` tags
- Maintain the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections: Use `#section-name`
2. For external pages: Replace with full URL
   ```html
   <a href="https://yoursite.com/page">Page Name</a>
   ```

### Call-to-Action Buttons
Current affiliate link:
```html
<a href="https://www.cloudways.com/en/?id=1384181" class="inline-block bg-blue-600...">
```
To update:
1. Replace the URL while maintaining the classes
2. Test the link before deploying
3. Keep the `inline-block` and other styling classes

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

To implement proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS and Alpine.js imports
3. Maintain consistent text styling:
```html
<main class="container mx-auto px-6 py-24">
    <h1 class="text-3xl md:text-4xl font-bold mb-8">Privacy Policy</h1>
    <div class="prose max-w-none">
        <!-- Your policy content here -->
    </div>
</main>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
- Check that you've maintained all responsive classes (md:, lg:)
- Verify Tailwind CSS is properly loaded
- Test on multiple screen sizes

2. **Missing Hover Effects**
- Ensure hover: classes remain intact
- Example: `hover:text-blue-600 hover:bg-gray-100`

3. **Inconsistent Spacing**
- Use Tailwind's spacing scale (m-4, p-6, etc.)
- Maintain existing margin/padding patterns

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all script and style imports are working
- Test all links before deploying changes
- Use browser developer tools to inspect elements

Remember to always backup your files before making significant changes, and test thoroughly on different devices and browsers.