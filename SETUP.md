# Jekyll Setup Instructions

## ✅ What's Been Configured

Your GitHub Pages site is now configured with:

- **Jekyll Theme**: Cayman (professional, clean design)
- **Mermaid Support**: All diagrams will render automatically
- **Custom Layout**: Enhanced typography and styling for academic papers
- **SEO**: Automatic meta tags and sitemap generation
- **Responsive**: Mobile-friendly design

## 🚀 Quick Start - GitHub Pages (Easiest)

1. Commit and push your changes:
   ```bash
   git add .
   git commit -m "Setup Jekyll with Mermaid support"
   git push origin main
   ```

2. Enable GitHub Pages:
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under "Build and deployment":
     - Source: **Deploy from a branch**
     - Branch: **main** / root
   - Click **Save**

3. Wait 1-2 minutes and visit your site at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/whitepaper.html
   ```

## 🧪 Local Testing (Optional)

To preview your site locally before pushing:

### Prerequisites
- Ruby 2.7+ ([Install Ruby](https://www.ruby-lang.org/en/documentation/installation/))
- Bundler (`gem install bundler`)

### Steps

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run Jekyll locally:
   ```bash
   bundle exec jekyll serve
   ```

3. Open in browser:
   ```
   http://localhost:4000/whitepaper.html
   ```

4. Make changes - Jekyll will auto-rebuild (refresh browser to see changes)

## 📁 File Structure

```
modular-architectures/
├── _config.yml              # Jekyll configuration
├── _layouts/
│   └── default.html         # Custom layout with Mermaid
├── assets/
│   └── css/
│       └── style.scss       # Custom styles
├── whitepaper.md            # Your whitepaper (main content)
├── index.html               # Redirects to whitepaper
├── CNAME                    # Custom domain (if configured)
├── Gemfile                  # Ruby dependencies
└── README.md                # Project documentation
```

## 🎨 Customization

### Change Theme Colors

Edit `_layouts/default.html` and modify the CSS variables:

```css
.main-content h2 {
  color: #159957; /* Change this color */
}
```

### Add Custom Domain

1. Add your domain to `CNAME` file:
   ```
   yourdomain.com
   ```

2. Configure DNS with your provider:
   - Add CNAME record pointing to `YOUR-USERNAME.github.io`

3. Enable HTTPS in GitHub Pages settings (automatic after DNS propagation)

### Modify Layout

- **Header**: Edit the `<header>` section in `_layouts/default.html`
- **Footer**: Edit the `<footer>` section
- **Styles**: Add custom CSS in the `<style>` block or `assets/css/style.scss`

## 📊 Mermaid Diagrams

Mermaid diagrams in your markdown will automatically render. Example:

```markdown
\`\`\`mermaid
graph LR
    A[Start] --> B[Process]
    B --> C[End]
\`\`\`
```

## 🐛 Troubleshooting

### Site not updating?
- Clear GitHub Pages cache (wait 5-10 min)
- Check GitHub Actions tab for build errors
- Verify branch is set correctly in Pages settings

### Mermaid not rendering?
- Check browser console for JavaScript errors
- Ensure code blocks use \`\`\`mermaid (not \`\`\`graph)
- Try clearing browser cache

### Local build fails?
```bash
# Update dependencies
bundle update

# Clean and rebuild
bundle exec jekyll clean
bundle exec jekyll serve
```

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Mermaid Documentation](https://mermaid.js.org/)
- [Cayman Theme](https://github.com/pages-themes/cayman)

## 📄 License

This setup is based on the Cayman theme (MIT License) and can be freely used and modified.

