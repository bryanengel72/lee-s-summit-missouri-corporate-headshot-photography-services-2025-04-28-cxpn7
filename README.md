# 101Headshots Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<span class="text-xl font-bold text-gray-900">101Headshots</span>
```
- Replace "101Headshots" with your company name
- Keep the surrounding classes to maintain styling

### Hero Section
Located at the top of the page with the main heading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Lee's Summit, Missouri Corporate Headshot Photography Services
</h1>
```
- Update the location and service description
- The classes ensure responsive text sizing:
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <!-- Icon container -->
    <div class="h-12 w-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text.</p>
</div>
```
To modify:
1. Change the title in the `<h3>` tag
2. Update the description in the `<p>` tag
3. Keep all classes to maintain styling and hover effects

### Working with Tailwind Classes
Common classes explained:
- `text-gray-600`: Text color
- `hover:text-gray-900`: Color on hover
- `transition-colors`: Smooth color transitions
- `duration-300`: Transition timing
- `rounded-md`: Rounded corners
- `shadow-lg`: Box shadow
- `hover:shadow-xl`: Larger shadow on hover

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="https://www.101headshots.com" class="inline-flex items-center...">Book Now</a>
</div>
```

To update links:
1. Internal links (starting with #) point to section IDs
2. External links (like Book Now) need full URLs
3. Update the `href` attribute with your new link
4. Example: `<a href="https://your-booking-site.com"`

### Footer Links
Located at the bottom of the page:
```html
<div class="text-lg font-semibold mb-4">Quick Links</div>
<ul class="space-y-2">
    <li><a href="#features" class="text-gray-400 hover:text-white transition duration-300">Features</a></li>
    <!-- More links -->
</ul>
```

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper paths:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from index.html
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match link hrefs
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Styling Issues**
   - Don't remove classes unless you're sure about their purpose
   - Keep responsive classes (md:, lg:) for proper mobile display
   - Test on different screen sizes after changes

3. **Layout Problems**
   - Maintain the grid structure in features section
   - Keep the `max-w-7xl` container for proper content width
   - Don't remove `px-4 sm:px-6 lg:px-8` padding classes

Need more help? Contact support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).