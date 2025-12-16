# Demo Collection

A GitHub Pages site showcasing HTML/CSS/JavaScript demonstrations with an attractive grid-based homepage.

## Structure

```
/
├── index.html          # Main homepage with demo grid
├── css/
│   └── main.css        # Styles for the homepage
├── demos/              # Directory containing all demos
│   ├── example-demo/   # Example demo template
│   │   ├── index.html  # Demo page
│   │   ├── style.css   # Demo styles
│   │   └── script.js   # Demo functionality
│   └── [your-demo]/    # Add new demos here
└── README.md
```

## Adding a New Demo

### Step 1: Create Demo Directory

Create a new folder in the `demos/` directory:

```bash
mkdir demos/your-demo-name
```

### Step 2: Create Demo Files

Copy the example demo structure or create three files:

1. **index.html** - Your demo page
2. **style.css** - Styling for your demo
3. **script.js** - JavaScript functionality

#### Recommended Template

Copy from the example demo:

```bash
cp -r demos/example-demo demos/your-demo-name
```

Then edit the files to create your demo.

#### Key Points

- Include a back navigation link: `<a href="../../index.html">Back to Home</a>`
- Keep the demo self-contained within its directory
- Use relative paths for assets
- Match the existing color scheme for consistency (optional)

### Step 3: Add Demo Card to Homepage

Edit `index.html` and add a new demo card to the grid:

```html
<a href="demos/your-demo-name/" class="demo-card">
    <div class="demo-card-content">
        <h2>Your Demo Title</h2>
        <p>Brief description of what your demo demonstrates.</p>
        <div class="demo-tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">JavaScript</span>
        </div>
    </div>
</a>
```

Add this inside the `<main class="demo-grid">` section, before the placeholder card.

## GitHub Pages Setup

### First Time Setup

1. Initialize git repository:
```bash
git init
git add .
git commit -m "Initial commit"
```

2. Create a GitHub repository and push:
```bash
git remote add origin https://github.com/yourusername/your-repo-name.git
git branch -M main
git push -u origin main
```

3. Enable GitHub Pages:
   - Go to your repository on GitHub
   - Navigate to Settings > Pages
   - Under "Source", select "Deploy from a branch"
   - Select the `main` branch and `/ (root)` folder
   - Click Save

Your site will be available at: `https://yourusername.github.io/your-repo-name/`

### Updating Your Site

After making changes:

```bash
git add .
git commit -m "Add new demo"
git push
```

GitHub Pages will automatically rebuild and deploy your site (usually takes 1-2 minutes).

## Design Features

- **Responsive Grid Layout**: Automatically adjusts from multi-column to single column on smaller screens
- **Dark Theme**: Modern dark color scheme with gradient accents
- **Interactive Cards**: Hover effects and smooth transitions
- **Clean Typography**: System font stack for optimal performance
- **Accessibility**: Semantic HTML and proper contrast ratios

## Customization

### Color Scheme

Edit the CSS variables in `css/main.css`:

```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    --background: #0f172a;
    --surface: #1e293b;
    --text-primary: #f1f5f9;
    --accent: #22d3ee;
}
```

### Homepage Title

Edit the header section in `index.html`:

```html
<header>
    <h1>Your Title Here</h1>
    <p class="subtitle">Your subtitle here</p>
</header>
```

## Tips

- Keep each demo self-contained in its own directory
- Use descriptive folder names (lowercase, hyphens for spaces)
- Test locally by opening `index.html` in a browser
- Remove the placeholder card from `index.html` once you have real demos
- Consider adding screenshots or GIFs to demo pages
- Add meta tags for better social sharing

## License

Feel free to use this template for your own projects.
