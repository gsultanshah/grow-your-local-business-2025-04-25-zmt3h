# OneCall Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the OneCall landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">OneCall</a>
```
- Replace "OneCall" with your company name
- Adjust text size using Tailwind classes:
  - `text-2xl` (current) = large
  - `text-xl` = smaller
  - `text-3xl` = larger

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Grow Your Local Business
</h1>
```
- Replace "Grow Your Local Business" with your headline
- Size classes explained:
  - `text-4xl` = mobile size
  - `md:text-5xl` = tablet size
  - `lg:text-6xl` = desktop size

### Features and Benefits Cards
Each card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class='bx bx-trending-up text-2xl text-blue-600'></i>
    </div>
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Growth Strategies</h3>
    <p class="text-gray-600 leading-relaxed">Implement proven growth strategies...</p>
</div>
```
To modify:
1. Change icon: Replace `bx-trending-up` with any [Boxicons](https://boxicons.com/) class
2. Update heading: Modify text in the `<h3>` tag
3. Update description: Modify text in the `<p>` tag

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Keep the `#` prefix
   - Ensure the ID matches a section (e.g., `id="features"`)
2. External links:
   - Replace `#section-name` with full URL
   - Example: `href="https://www.example.com/page"`

### Call-to-Action Buttons
```html
<a href="https://www.onecallapp.com" class="inline-flex items-center...">
    Start Growing Today
</a>
```
- Replace `https://www.onecallapp.com` with your target URL
- Update button text between opening and closing tags

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add these links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Add this code before the closing `</div>` in the footer grid.

### Step 2: Create Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use this basic template for each:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy | OneCall</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased text-gray-800 bg-white">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 py-32">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Check mobile-first classes (without prefix)
   - Then check responsive breakpoints (`sm:`, `md:`, `lg:`)
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Icons Not Showing**
   - Verify Boxicons CSS is loaded
   - Check icon class names on [Boxicons](https://boxicons.com/)
   - Ensure `bx` prefix is included

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or [Boxicons documentation](https://boxicons.com/).