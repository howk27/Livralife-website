# Livra+ Marketing Website

A complete, static marketing website for the Livra+ mobile app. This is a production-ready static site that can be deployed to Vercel or any static hosting service.

## What This Is

This is a minimalist, dark-themed marketing website for Livra+, a habit tracking mobile app. The site includes:

- Home page with hero, features overview, and preview sections
- Features page with detailed feature descriptions
- App preview gallery
- Support/verification page (for Apple App Store requirements)
- Privacy policy and terms of service pages
- Contact page
- 404 error page

## Technology Stack

- **HTML5** - Semantic markup
- **CSS3** - Custom CSS with CSS variables for theming
- **Vanilla JavaScript** - Minimal JS for mobile navigation only
- **No frameworks** - Pure static site, no build step required

## Project Structure

```
/website
  /assets
    /images      # Placeholder for images
    /ui          # Placeholder for UI screenshots
  /css
    styles.css   # All styles in one file
  /js
    main.js      # Mobile navigation toggle
  index.html     # Home page
  features.html  # Features page
  preview.html   # UI gallery
  verification.html  # Support/verification page
  privacy.html   # Privacy policy
  terms.html     # Terms of service
  contact.html   # Contact page
  404.html       # 404 error page
  robots.txt     # SEO robots file
  sitemap.xml    # SEO sitemap
  README.md      # This file
```

## Running Locally

### Option 1: Open Directly
Simply open `index.html` in your web browser. Note that some features may be limited without a local server.

### Option 2: Simple Local Server

**Python 3:**
```bash
cd website
python -m http.server 8000
```
Then visit `http://localhost:8000`

**Node.js (with http-server):**
```bash
cd website
npx http-server -p 8000
```
Then visit `http://localhost:8000`

**PHP:**
```bash
cd website
php -S localhost:8000
```
Then visit `http://localhost:8000`

## Deployment to Vercel

### Method 1: Vercel CLI

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Navigate to the website directory:
```bash
cd website
```

3. Deploy:
```bash
vercel
```

4. Follow the prompts to link your project or create a new one.

### Method 2: Vercel Dashboard

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "New Project"
3. Import your Git repository (or drag and drop the `/website` folder)
4. Set the **Root Directory** to `website`
5. Deploy

### Method 3: Git Integration

1. Push your code to GitHub/GitLab/Bitbucket
2. Connect your repository to Vercel
3. Set the **Root Directory** to `website`
4. Deploy

## Domain Setup (livralife.com)

After deploying to Vercel:

1. Go to your project settings in Vercel
2. Navigate to "Domains"
3. Add `livralife.com` and `www.livralife.com`
4. Update your DNS records as instructed by Vercel:
   - Add a CNAME record pointing to Vercel's provided domain
   - Or add A records if using apex domain

### DNS Configuration

For `livralife.com` (apex domain):
- Type: A
- Value: Vercel's IP addresses (provided in dashboard)

For `www.livralife.com`:
- Type: CNAME
- Value: `cname.vercel-dns.com`

## Design System

### Color Palette

The site uses a dark theme by default with CSS variables defined in `styles.css`. All colors follow the Livra+ brand guidelines:

- **Background**: Dark green (#1F2E2C)
- **Surface**: Darker green (#2B3A39)
- **Primary Accent**: Muted coral (#D8A7A0)
- **Text**: Light beige (#F3F1EB)

See `css/styles.css` for the complete color system.

### Typography

- Font stack: `ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial`
- Responsive font sizes using CSS variables
- Strong hierarchy with clear heading styles

## Adding Images

To add screenshots or images:

1. Place UI screenshots in `/website/assets/ui/`
2. Place other images in `/website/assets/images/`
3. Update the HTML to reference the images:
   ```html
   <img src="assets/ui/screenshot-1.png" alt="Description">
   ```

Currently, the site uses placeholder divs that can be easily replaced with `<img>` tags.

## Contact Form

The contact form currently uses a `mailto:` link as a fallback. For production, consider integrating:

- **Wix Forms** - If using Wix
- **Formspree** - Simple form backend
- **Netlify Forms** - If deploying to Netlify
- **Vercel Serverless Functions** - For custom backend

To integrate a form service, replace the form submission handler in `contact.html`.

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Responsive design works on all screen sizes

## Accessibility

- Semantic HTML5 elements
- ARIA labels on interactive elements
- Keyboard navigation support
- Focus states for all interactive elements
- Proper color contrast ratios
- Screen reader friendly

## License

This website is part of the Livra+ project. All rights reserved.

## Support

For questions about this website, contact:
- **Email**: support@livralife.com
- **Website**: livralife.com

