# Legal Documents for STRIPED

This directory contains the Privacy Policy and Terms of Service for the STRIPED golf training app.

## Files

- **PRIVACY_POLICY.md** - Explains what data we collect and how we use it
- **TERMS_OF_SERVICE.md** - Legal terms governing use of the app

## Required Actions Before Launch

### 1. ✅ Contact Email Updated
All instances updated to: jacob@smallstack.co

### 2. ✅ Jurisdiction Updated
Set to: United States and the State of Indiana

### 3. Host Publicly

These documents must be accessible via public URLs for App Store submission. Options:

#### Option A: GitHub Pages (Recommended - Free & Easy)
1. Create a new repository: `striped-legal` or use `stripedgolf.github.io`
2. Upload both markdown files or convert to HTML
3. Enable GitHub Pages in repository settings
4. URLs will be: 
   - `https://yourusername.github.io/striped-legal/PRIVACY_POLICY.html`
   - `https://yourusername.github.io/striped-legal/TERMS_OF_SERVICE.html`

#### Option B: AWS S3 Static Website
1. Create an S3 bucket (e.g., `striped-legal-docs`)
2. Enable static website hosting
3. Upload HTML versions of the documents
4. Make bucket publicly readable
5. Optional: Add CloudFront for HTTPS

#### Option C: Simple Web Host
- Upload to any web hosting service (Netlify, Vercel, etc.)
- Ensure HTTPS is enabled

### 4. Link in App

Add links to these documents in your app:
- Profile/Settings screen
- Login/Signup flow footer
- Onboarding screens

Example code for ProfileScreen:
```typescript
<TouchableOpacity onPress={() => Linking.openURL('https://your-domain.com/privacy')}>
  <Text>Privacy Policy</Text>
</TouchableOpacity>
<TouchableOpacity onPress={() => Linking.openURL('https://your-domain.com/terms')}>
  <Text>Terms of Service</Text>
</TouchableOpacity>
```

### 5. App Store Submission Fields

When submitting to App Stores, you'll need to provide these URLs:

**Apple App Store Connect:**
- Privacy Policy URL: `https://...`
- Terms of Service URL (optional but recommended): `https://...`

**Google Play Console:**
- Privacy Policy URL: `https://...` (required)

## Converting Markdown to HTML

If hosting on a platform that doesn't support Markdown:

### Using Pandoc (command line):
```bash
pandoc PRIVACY_POLICY.md -o privacy-policy.html -s --metadata title="Privacy Policy"
pandoc TERMS_OF_SERVICE.md -o terms-of-service.html -s --metadata title="Terms of Service"
```

### Using Online Tools:
- [Markdown to HTML](https://markdowntohtml.com/)
- [Dillinger.io](https://dillinger.io/)

### Manual HTML Template:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - STRIPED Golf Training</title>
    <style>
        body { max-width: 800px; margin: 40px auto; padding: 0 20px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; line-height: 1.6; }
        h1 { border-bottom: 2px solid #16a34a; padding-bottom: 10px; }
        h2 { color: #16a34a; margin-top: 30px; }
        a { color: #16a34a; }
    </style>
</head>
<body>
    <!-- Paste converted HTML content here -->
</body>
</html>
```

## Legal Review (Recommended)

While these documents are comprehensive and follow industry standards:
- Consider having a lawyer review them before launch if possible
- They are written in clear, user-friendly language (required by GDPR/CCPA)
- They cover standard scenarios for a mobile training app

## Maintenance

Update these documents when:
- You add new features that collect different data
- You introduce payment processing or subscriptions
- You start using third-party analytics or tracking tools
- Laws or regulations change

Always update the "Last Updated" date at the top when making changes.

## Questions?

These documents are designed to:
- ✅ Comply with App Store requirements
- ✅ Meet GDPR and CCPA standards
- ✅ Protect both users and the company
- ✅ Be clear and readable (not just legal jargon)

If you have specific legal questions, consult with a lawyer in your jurisdiction.
