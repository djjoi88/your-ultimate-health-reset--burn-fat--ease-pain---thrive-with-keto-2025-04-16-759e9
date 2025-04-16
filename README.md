# LifeWave Fitness Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the LifeWave Fitness landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Navigation Links](#managing-navigation-links)
3. [Setting Up Legal Pages](#setting-up-legal-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this line in the header:
```html
<div class="text-xl font-bold text-gray-800">LifeWave Fitness</div>
```
Simply replace "LifeWave Fitness" with your brand name.

### Hero Section
The hero section is your main banner. To modify:

1. **Main Headline**: Find:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Your Ultimate Health Reset: Burn Fat, Ease Pain & Thrive with Keto
</h1>
```
Replace the text between the `<h1>` tags with your headline.

2. **Subheadline**: Locate:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Unlock Effortless Weight Loss & Pain Relief!
</p>
```
Update the text between the `<p>` tags.

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `font-bold`: Bold text
- `mb-8`: Margin bottom spacing
- `bg-white`: White background
- `hover:text-blue-600`: Blue text on hover

To modify styling, adjust these classes. For example:
```html
<!-- Original -->
<div class="text-xl font-bold text-gray-800">

<!-- Make text larger and red -->
<div class="text-2xl font-bold text-red-800">
```

## Managing Navigation Links

### Main Navigation
The navigation menu is in the header section:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. The `href="#features"` format links to sections within the page
2. For external links, use full URLs: `href="https://yoursite.com/page"`
3. Ensure section IDs match your href values

### Call-to-Action Buttons
Update the main CTA links:

```html
<!-- Hero CTA -->
<a href="https://lifewavefitness.com/keto-conv" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```

Replace `https://lifewavefitness.com/keto-conv` with your destination URL.

## Setting Up Legal Pages

### Footer Legal Links
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create two new files:
   - `privacy.html`
   - `terms.html`

2. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying the header and footer from index.html to your new pages.

## Troubleshooting

Common issues and solutions:

### Links Not Working
- Check that href values exactly match section IDs
- Ensure external URLs include `https://`
- Verify file names and paths are correct

### Styling Issues
- Make sure Tailwind CSS is properly loaded
- Check for typos in class names
- Maintain responsive classes (md:, lg:) for different screen sizes

### Text Not Updating
- Look for closing tags (`</div>`, `</p>`, etc.)
- Check for special characters that might break HTML
- Verify changes are saved and files are uploaded

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).