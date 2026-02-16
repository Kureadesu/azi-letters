# Azi Letters - Personal Journal Website

A beautiful, intimate static website for personal letters and reflections. Designed with a warm, journal-like aesthetic featuring elegant typography, soft colors, and thoughtful animations.

## 🎨 Design Features

- **Distinctive Typography**: Cormorant Garamond for display, Crimson Pro for body text, and Jost for UI elements
- **Warm Color Palette**: Cream, parchment, soft rose, and terracotta tones
- **Paper-Like Aesthetic**: Subtle textures and shadows that evoke handwritten letters
- **Smooth Animations**: Fade-in effects and hover states for an engaging experience
- **Fully Responsive**: Looks beautiful on desktop, tablet, and mobile devices
- **Accessibility**: Keyboard navigation support and reduced motion preferences

## 📁 File Structure

```
azi-letters/
├── index.html              # Home page with dedication
├── letters.html            # List of all letters
├── css/
│   └── style.css          # All styling (typography, colors, layout, animations)
├── letters/
│   ├── letter1.html       # Individual letter page
│   ├── letter2.html       # Individual letter page
│   ├── letter3.html       # Individual letter page
│   └── ...                # Add more letters here
└── images/                # Optional folder for images
```

## 🚀 Getting Started

### Option 1: Open Locally
1. Download all files
2. Open `index.html` in your web browser
3. Navigate through the site using the navigation menu

### Option 2: Host on GitHub Pages (Free)
1. Create a new GitHub repository
2. Upload all files to the repository
3. Go to Settings → Pages
4. Select "main" branch as source
5. Your site will be live at `https://yourusername.github.io/repository-name/`

### Option 3: Host on Netlify (Free)
1. Sign up at [netlify.com](https://netlify.com)
2. Drag and drop your entire `azi-letters` folder
3. Your site goes live instantly with a custom URL

## ✍️ Adding New Letters

### Step 1: Create the Letter Page

1. **Duplicate an existing letter** (e.g., `letter3.html`) in the `letters/` folder
2. **Rename it** to `letter4.html` (or next number)
3. **Update the content**:
   - Change the `<title>` tag
   - Update the date in `datetime` attribute
   - Change the heading `<h1>`
   - Replace the letter body with your content

Example structure:
```html
<article class="letter-content">
  <header class="letter-header">
    <h1>Your Letter Title</h1>
    <time class="letter-date" datetime="2026-02-20">February 20, 2026</time>
  </header>
  
  <div class="letter-body">
    <p>First paragraph...</p>
    <p>Second paragraph...</p>
    <!-- Add more paragraphs as needed -->
  </div>
</article>
```

### Step 2: Add to Letters List

1. Open `letters.html`
2. **Add a new letter card** in the `letters-grid` section:

```html
<article class="letter-card">
  <div class="letter-meta">February 20, 2026</div>
  <h3>Your Letter Title</h3>
  <p class="excerpt">
    A brief excerpt or preview of your letter (2-3 sentences)...
  </p>
  <a href="letters/letter4.html" class="read-more">Read Letter →</a>
</article>
```

3. Save and refresh your browser!

## 🎨 Customization Guide

### Change Colors

Open `css/style.css` and modify the CSS variables at the top:

```css
:root {
  --color-cream: #faf7f2;        /* Background color */
  --color-soft-rose: #e8b4a8;    /* Accent color */
  --color-terracotta: #c17a6f;   /* Links and highlights */
  --color-deep-brown: #5a4a42;   /* Headings */
  --color-ink: #3d3230;          /* Body text */
}
```

### Change Fonts

The website uses three font families from Google Fonts:
- `Cormorant Garamond` - Display/headings
- `Crimson Pro` - Body text
- `Jost` - UI elements

To change fonts:
1. Visit [Google Fonts](https://fonts.google.com)
2. Select your preferred fonts
3. Copy the `<link>` tag
4. Replace the font link in all HTML files
5. Update the CSS variables in `style.css`:

```css
--font-display: 'Your Display Font', serif;
--font-body: 'Your Body Font', serif;
--font-ui: 'Your UI Font', sans-serif;
```

### Modify the Dedication Text

Open `index.html` and find the `.dedication` section:

```html
<div class="dedication">
  <p>
    Your personalized dedication text here...
  </p>
</div>
```

### Change the Website Name

Replace "Azi Letters" throughout all HTML files:
- Navigation brand (`nav-brand`)
- Page titles (`<title>` tags)
- Any references in content

## 📱 Mobile Responsive

The website automatically adapts to different screen sizes:
- **Desktop**: Full layout with generous spacing
- **Tablet**: Adjusted padding and font sizes
- **Mobile**: Optimized for small screens with readable text

No additional configuration needed!

## ♿ Accessibility Features

- Semantic HTML structure
- Keyboard navigation support
- Focus indicators for interactive elements
- Respects `prefers-reduced-motion` for users who need it
- High contrast text for readability
- ARIA labels where appropriate

## 💡 Tips & Best Practices

### Writing Letters
- Use paragraphs (`<p>` tags) to structure your content
- The first paragraph automatically gets a decorative drop cap
- Keep line length comfortable (already optimized in CSS)
- Use meaningful titles that reflect the letter's content

### Organizing Letters
- Number your letters sequentially (letter1, letter2, etc.)
- Add the newest letters at the **top** of `letters.html` for easy access
- Include dates to create a timeline
- Write meaningful excerpts that entice reading

### Performance
- The website loads quickly (no external dependencies except fonts)
- All animations are CSS-based for smooth performance
- Images are optional and can be added to the `images/` folder

### Privacy
- This is a static website with no tracking or analytics
- No data is collected or sent anywhere
- Host it privately if you want complete control
- Consider password-protecting via hosting provider settings

## 🔒 Making It Private

### Option 1: Password Protection (Netlify)
1. In Netlify dashboard, go to Site Settings
2. Access Control → Visitor Access
3. Set a password for your site

### Option 2: Hidden Repository (GitHub)
1. Make your repository private
2. Only deploy to GitHub Pages if comfortable with public access

### Option 3: Local Only
- Keep the files on your computer
- Open directly in browser when you want to read/write
- No internet hosting required

## 🎯 Common Customizations

### Change Navigation Links
Edit the `<nav>` section in each HTML file:
```html
<ul class="nav-links">
  <li><a href="index.html">Home</a></li>
  <li><a href="letters.html">Letters</a></li>
  <!-- Add more links here -->
</ul>
```

### Add Images to Letters
```html
<div class="letter-body">
  <p>Your text...</p>
  <img src="../images/your-image.jpg" alt="Description" 
       style="width: 100%; border-radius: 8px; margin: 2rem 0;">
  <p>More text...</p>
</div>
```

### Change Footer Text
Edit the `<footer>` section in each HTML file:
```html
<footer>
  <p>Your custom footer text</p>
</footer>
```

## 🐛 Troubleshooting

**Links not working?**
- Check that file paths are correct (relative to current file)
- From `letters/letter1.html`, use `../letters.html` to go back up

**Fonts not loading?**
- Ensure you're connected to the internet (fonts load from Google)
- Check that the font link in `<head>` is correct

**Styling looks broken?**
- Verify that `style.css` is in the `css/` folder
- Check that the link to CSS is correct in each HTML file

**Website not showing on hosting?**
- Ensure `index.html` is in the root folder
- Wait a few minutes for hosting to deploy
- Check hosting provider's status/logs

## 📝 License

This is your personal project! Feel free to modify, customize, and use it however you like.

## 💖 Final Notes

This website is designed to be a sacred space for your words. Take your time with it, make it yours, and let it evolve as your journey continues. Each letter you add becomes part of a larger tapestry—a testament to love, memory, and the power of written word.

The design intentionally feels handcrafted and warm because some things are too precious for cold, generic templates. Your letters deserve a home that honors their intimacy and importance.

---

**Need help?** The code is fully commented and organized for easy modification. Don't be afraid to experiment—you can always save backups before making changes!