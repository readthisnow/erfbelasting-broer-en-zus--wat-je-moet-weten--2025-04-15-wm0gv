# Landing Page Maintenance Guide

This guide will help you maintain and customize your NotarisOnline landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-900">Notaris<span class="text-blue-600">Online</span></a>
```
- Change "Notaris" and "Online" to your desired text
- Keep the `<span>` tag to maintain the two-color effect

2. **Navigation Menu Items:**
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600">Voordelen</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600">Contact</a>
</div>
```
- Replace "Voordelen", "FAQ", and "Contact" with your preferred menu items
- Keep the `hover:text-blue-600` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Erfbelasting Broer en Zus: <span class="text-blue-600">Wat je MOET weten!</span>
</h1>
```
- Update the heading text while maintaining the `<span>` for the highlighted portion
- The classes control size (`text-4xl`), spacing (`mb-8`), and color (`text-gray-900`)

### Understanding Tailwind Classes
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[number]`: Adds margin bottom (4, 8, 12, etc.)
- `py-[number]`: Adds padding top and bottom
- `px-[number]`: Adds padding left and right
- `bg-[color]`: Sets background color

## Managing Links

### Navigation Links
1. **Internal Links:**
```html
<a href="#features">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- The `#` symbol links to sections with matching IDs on the same page
- Ensure section IDs match exactly (case-sensitive)

2. **Call-to-Action Button:**
```html
<a href="https://notarissen-online.nl/zun" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Direct Regelen
</a>
```
- Replace the URL with your actual booking or contact page
- Keep the classes for consistent button styling

### Email Links
```html
<a href="mailto:info@notaris1.nl">info@notaris1.nl</a>
```
- Update both the `href` and displayed email to your business email
- Format: `mailto:your-email@domain.com`

## Adding Privacy and Terms Pages

### Footer Links Setup
1. Locate the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
</ul>
```

2. Update the placeholder links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Algemene Voorwaarden</a></li>
```

3. Create matching HTML files:
- Create `privacy.html` and `terms.html` in the same folder as `index.html`
- Use the same header and footer structure for consistency
- Add your policy content in the main section

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match the href attributes exactly
- Example: `href="#features"` must match `id="features"`
- IDs are case-sensitive

2. **Responsive Design Issues**
- Keep the responsive classes intact:
  ```html
  text-4xl md:text-5xl lg:text-6xl
  ```
- These control appearance at different screen sizes:
  - Default (mobile): `text-4xl`
  - Medium screens (`md:`): `text-5xl`
  - Large screens (`lg:`): `text-6xl`

3. **Missing Styles**
- Ensure the Tailwind CSS link remains in the header:
  ```html
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  ```
- Check for typos in class names

Remember to test all changes across different devices and browsers to ensure consistent appearance and functionality.