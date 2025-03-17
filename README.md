# Landing Page Maintenance Guide

This guide will help you maintain and customize the Valdeno.re landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Valdeno.re  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Fonctionnalités</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Avantages</a>
</div>
```

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Un site moderne & intelligent pour votre entreprise  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Création de sites web dynamiques avec chatbot IA intégré  <!-- Subheadline -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-gray-300`: Light gray text
- `hover:text-white`: Text becomes white on hover
- `md:text-5xl`: Text size changes at medium breakpoint
- `bg-gradient-to-r`: Right-directed gradient background
- `transition-colors`: Smooth color transitions

## Managing Links

### Navigation Links
Current navigation links are:

```html
<!-- In the header -->
<a href="#features">Fonctionnalités</a>
<a href="#benefits">Avantages</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- To update a link -->
<a href="#new-section">New Section Name</a>
```

### External Links
Update these important external links:

```html
<!-- Call-to-action button -->
<a href="https://contact.valdeno.re/" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Découvrir nos solutions
</a>

<!-- Email link -->
<a href="mailto:contact@valdeno.re">contact@valdeno.re</a>
```

## Adding Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Légal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Mentions légales</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
    </ul>
</div>
```

To add new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes as shown above
3. Ensure consistent styling by copying the class attributes

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all href attributes start with `/` for root-relative paths
   - Verify file names match exactly (case-sensitive)
   - Test all links after updating

2. **Responsive Design**
   - Classes starting with `md:` affect screens ≥768px wide
   - Classes starting with `lg:` affect screens ≥1024px wide
   - Always test on multiple device sizes after making changes

3. **Gradient Text Not Showing**
   - Ensure these three classes are present together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Style Maintenance Tips

1. Keep consistent colors:
   - Purple gradient: `from-purple-500 to-pink-500`
   - Text colors: `text-gray-300`, `text-gray-400`
   - Background: `bg-gray-900`, `bg-gray-800`

2. Maintain spacing consistency:
   - Vertical padding: `py-24`
   - Horizontal padding: `px-4`
   - Container class: `container mx-auto`

Remember to always test your changes in multiple browsers and device sizes before deploying to production.