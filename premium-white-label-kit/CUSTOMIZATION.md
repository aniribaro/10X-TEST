# White-Label Customization Guide

## Premium Feature - For Paying Customers Only

This guide shows you how to fully rebrand 10X Accountability Coach as your own product.

---

## Quick Start

### 1. Edit `branding.json`

Open `branding.json` and update:

```json
{
  "appName": "Your App Name",
  "tagline": "Your custom tagline",
  "logo": "/path/to/your-logo.svg",
  "colors": {
    "primary": "#your-hex-color",
    "secondary": "#your-hex-color"
  }
}
```

### 2. Replace Logo

Place your logo in:
- `ui/public/logo.svg` (main app logo)
- `docs/assets/logo.svg` (landing page logo)

Recommended format: SVG (scalable)
Recommended size: 200x50px

### 3. Update Colors

Edit `ui/tailwind.config.js`:

```js
theme: {
  extend: {
    colors: {
      'oa-accent': '#YOUR_PRIMARY_COLOR',
      'oa-accent-soft': '#YOUR_SECONDARY_COLOR',
    }
  }
}
```

### 4. Update Landing Page

Edit `docs/index.html`:

1. Replace all instances of "10X Accountability Coach" with your app name
2. Update the tagline
3. Replace logo references
4. Update footer credits (keep "Powered by OpenAnalyst" or upgrade to Enterprise to remove)

### 5. Update App Meta Tags

Edit `ui/app/layout.tsx`:

```tsx
export const metadata: Metadata = {
  title: 'Your App Name',
  description: 'Your custom description',
}
```

---

## Color Customization

### Default Theme Colors

```css
--oa-accent: #8b5cf6        /* Primary purple */
--oa-accent-soft: #a78bfa    /* Light purple */
--oa-bg-primary: #0a0a0f     /* Dark background */
--oa-bg-secondary: #111118   /* Card background */
--oa-border: rgba(255,255,255,0.1)
```

### Creating Your Theme

1. Choose a primary brand color
2. Generate a color palette at https://coolors.co or https://paletton.com
3. Replace colors in:
   - `ui/tailwind.config.js`
   - `docs/styles.css` (CSS variables at top)

---

## Logo Guidelines

### Requirements
- Format: SVG preferred (PNG acceptable)
- Dimensions: Max 200px wide
- Background: Transparent
- Colors: Works on dark background (#0a0a0f)

### Placement
| Location | File Path | Usage |
|----------|-----------|-------|
| Main App | `ui/public/logo.svg` | Header, loading |
| Landing Page | `docs/assets/logo.svg` | Hero section |
| Favicon | `ui/app/favicon.ico` | Browser tab |
| OG Image | `docs/assets/og-image.png` | Social sharing |

---

## Domain Setup

### Custom Domain with Vercel

1. Add domain in Vercel dashboard
2. Update DNS records
3. SSL is automatic

### Custom Domain with Hostinger

1. Point A record to your server IP
2. Add CNAME for www subdomain
3. Configure SSL certificate

---

## Email Branding

Update the email in `docs/script.js`:

```javascript
const yourEmail = 'support@yourdomain.com';
```

---

## Tier Comparison

| Feature | Free | Pro ($9/mo) | Enterprise ($99/mo) |
|---------|------|-------------|---------------------|
| Basic customization | No | Yes | Yes |
| Color themes | No | Yes | Yes |
| Custom logo | No | Yes | Yes |
| Remove "Powered by" | No | No | Yes |
| Priority support | No | Yes | Yes |
| Source code access | No | No | Yes |
| Multiple instances | No | No | Yes |

---

## Support

For white-label support, contact: anit.c@openanalyst.com

Include:
- Your order/transaction ID
- Screenshot of issue
- Description of customization needed

---

*Premium White-Label Kit - 10X Accountability Coach by Team 10X*
