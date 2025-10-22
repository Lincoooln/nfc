# The Book of Answers - NFC Divination Website

A beautiful, mobile-responsive single-page web application that displays random divination answers. Perfect for NFC tags that open directly to inspirational guidance.

## Features

- **Beautiful Card Design**: Clean, modern card-based UI with gradient backgrounds
- **Smooth Animations**: Floating particles, fade-in effects, and shimmer animations
- **Mobile Optimized**: Fully responsive design that works perfectly on all screen sizes
- **Bilingual Support**: Switch between English and Chinese (中文)
- **Fast Loading**: Single HTML file with no external dependencies
- **Interactive**: Tap anywhere on the card or use the button to get a new answer
- **NFC Ready**: Instant loading, perfect for NFC tag experiences

## Quick Start

### Local Testing

1. Simply open `index.html` in any web browser
2. That's it! No build process or server required

### Customizing the Answers

Open `index.html` and find the `answers` object (around line 268):

```javascript
const answers = {
    en: [
        "Yes, definitely.",
        "Trust your intuition.",
        // ... add your answers here
    ],
    zh: [
        "是的，毫无疑问。",
        "相信你的直觉。",
        // ... add Chinese translations here
    ]
};
```

Replace the sample answers with your own content from "The Book of Answers" or any other source.

## Deployment

### GitHub Pages (Recommended)

1. Create a new GitHub repository
2. Upload `index.html` to the repository
3. Go to Settings → Pages
4. Select "main" branch as source
5. Your site will be live at `https://yourusername.github.io/repository-name/`

See `deployment-guide.md` for detailed step-by-step instructions.

### Other Hosting Options

This single HTML file can be deployed to:
- **Netlify**: Drag and drop the file
- **Vercel**: Upload via CLI or web interface
- **Any web hosting**: Upload via FTP
- **Local server**: Works with any HTTP server

## NFC Setup

To create an NFC tag that opens this website:

1. Deploy the website and get your URL
2. Use an NFC writing app on your phone
3. Write the URL to your NFC tag
4. Test by tapping the tag with your phone

See `nfc-setup-guide.md` for detailed NFC hardware setup instructions.

## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge (recommended)
- Safari (iOS and macOS)
- Firefox
- Opera

## Customization Tips

### Change Colors

Find the gradient in the `body` style (around line 19):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Adjust Font

Change the font-family in the `body` style:
```css
font-family: 'Georgia', serif;
```

### Modify Animation Speed

Adjust animation durations in the CSS:
- Particle float: `animation: float 15s infinite;`
- Card fade-in: `animation: fadeIn 1s ease-out;`
- Answer slide-in: `animation: slideIn 0.8s ease-out;`

## Technical Details

- **Size**: ~10KB (single HTML file)
- **Dependencies**: None (pure HTML/CSS/JavaScript)
- **Load Time**: Instant (no external resources)
- **Performance**: Optimized with CSS animations and minimal JavaScript

## License

This template is free to use. Add your own content and customize as needed.

## Support

For issues or questions about:
- Deployment: See `deployment-guide.md`
- NFC setup: See `nfc-setup-guide.md`
- Customization: Edit the HTML file directly

---

Made with ❤️ for divination and inspiration
