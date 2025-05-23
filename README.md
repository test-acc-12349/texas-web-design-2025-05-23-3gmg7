# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- CTA Section
- Footer

### Updating Text Content

#### Hero Section
To update the main headline and subheading:
```html
<!-- Find this section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Best Websites In Texas</p>

<!-- Replace the text between the tags -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Your New Headline</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Your New Subheading</p>
```

#### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-server text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Reliable and secure hosting included with every website package.</p>
</div>
```

To update a feature:
1. Locate the feature card you want to change
2. Update the icon by changing the `fa-server` class to another [Font Awesome icon](https://fontawesome.com/icons)
3. Modify the heading text in the `<h3>` tag
4. Update the description in the `<p>` tag

### Understanding Tailwind CSS Classes

Key class patterns used in this landing page:

#### Spacing Classes
- `px-6`: Padding left and right
- `py-4`: Padding top and bottom
- `mb-6`: Margin bottom
- `space-x-8`: Horizontal spacing between elements

#### Responsive Classes
- `md:text-5xl`: Applies at medium screens and up
- `lg:text-6xl`: Applies at large screens and up
- `hidden md:flex`: Hidden on mobile, flex on medium screens

#### Color Classes
- `text-blue-600`: Blue text
- `bg-white`: White background
- `hover:bg-blue-700`: Background changes to darker blue on hover

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update a link:
1. Find the `<a>` tag you want to modify
2. Change the `href` attribute to your new destination
3. Update the text between the tags
4. Keep the existing classes to maintain styling

### External Links
The following links need to be updated with your actual domain:
```html
<!-- Header "Get Started" button -->
<a href="https://twd.com" class="hidden md:inline-block px-6 py-2 bg-blue-600 text-white rounded-full">Get Started</a>

<!-- Hero section button -->
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>

<!-- CTA section button -->
<a href="https://twd.com" class="inline-block px-8 py-4 bg-white text-blue-600 rounded-full">Contact Us Today</a>
```

## Adding Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages
1. Create new files:
   - Create `privacy.html` in your root directory
   - Create `terms.html` in your root directory

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and hrefs
   - Verify file paths are correct relative to index.html

2. **Responsive Design Issues**
   - Check that `md:` and `lg:` classes are properly set
   - Verify the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Icons Not Showing**
   - Confirm Font Awesome CSS is properly linked
   - Check for correct icon class names
   - Verify internet connection for CDN access

4. **Styling Inconsistencies**
   - Ensure Tailwind CSS CDN is properly loaded
   - Check for missing closing tags
   - Verify class names are spelled correctly

For additional help or more complex customizations, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or seek professional assistance.