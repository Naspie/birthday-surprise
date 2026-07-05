# 🎨 Customization Guide

## Quick Start Customization

### 1. Change the Passcode

Open `index.html` and find line ~187:

```javascript
const CORRECT_PASSCODE = "1234"; // Change this!
```

Replace `"1234"` with any 4-digit code you want. Examples:
- `"0705"` for July 5th
- `"1988"` for birth year
- `"2023"` for current year

### 2. Update the Birthday Message

Find this line (around line 189):

```javascript
const CUSTOM_MESSAGE = "Wishing you a day filled with joy, laughter, and unforgettable moments! May all your dreams come true today and always!";
```

Replace with your custom message. Examples:
- "Happy Birthday Alex! 🥳 You're officially 30!"
- "Mom, hope this day is as special as you are!"
- "🎂 You're aging like fine wine! Happy Birthday! 🍷"

### 3. Change the Birthday Photo

Find this line in the HTML (around line 111):

```html
<img src="https://images.unsplash.com/photo-1559827260-dc66d52bef19?w=400&h=400&fit=crop" alt="Birthday Person" class="login-photo">
```

**Option A: Use a local image**
```html
<img src="./birthday-photo.jpg" alt="Birthday Person" class="login-photo">
```

**Option B: Use an online image URL**
- Find an image URL (e.g., from Google Images, Unsplash, Pexels)
- Replace the `src` value

### 4. Customize Colors

#### Change the gradient background

Find in CSS (around line 23):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Color code examples:
- Purple to Pink: `linear-gradient(135deg, #667eea 0%, #d946ef 100%)`
- Blue to Cyan: `linear-gradient(135deg, #0ea5e9 0%, #06b6d4 100%)`
- Orange to Red: `linear-gradient(135deg, #f97316 0%, #dc2626 100%)`
- Green to Teal: `linear-gradient(135deg, #10b981 0%, #14b8a6 100%)`

#### Change confetti colors

Find this line (around line 260):
```javascript
const colors = ['#ff6b6b', '#feca57', '#48dbfb', '#1dd1a1', '#a29bfe', '#fd79a8', '#fdcb6e', '#6c5ce7'];
```

Add or replace hex color codes.

### 5. Customize Animations

#### Speed up/slow down animations

Find animation durations in CSS:

```css
animation: bounce 1s ease-in-out infinite;  /* Change 1s to 0.5s or 2s */
animation: confettiFall 3s linear infinite;  /* 3s duration */
```

Longer = slower (e.g., `2s`, `3s`, `4s`)
Shorter = faster (e.g., `0.5s`, `0.3s`)

### 6. Add Your Own Emojis

Find this line (around line 267):
```javascript
const emojis = ['🎉', '🎈', '🎂', '🎁', '🎊', '⭐', '✨', '🌟'];
```

Add more emojis:
```javascript
const emojis = ['🎉', '🎈', '🎂', '🎁', '🎊', '⭐', '✨', '🌟', '🎀', '💝', '🏆', '👑'];
```

### 7. Increase Confetti Amount

Find this line (around line 244):
```javascript
const confettiCount = 100;  // Change this number
```

- Higher number = more confetti (but may slow down on old devices)
- Try: `50`, `100`, `150`, `200`

### 8. Change Cake Design

#### Cake color
Find in CSS (around line 381):
```css
background: linear-gradient(to right, #d4a574 0%, #f4d4a6 50%, #d4a574 100%);
```

Change colors for different cake types:
- Chocolate: `#8b4513 0%, #a0522d 50%, #8b4513 100%`
- Vanilla: `#f5deb3 0%, #fffacd 50%, #f5deb3 100%`

#### Frosting color
Find in CSS (around line 405):
```css
background: linear-gradient(to bottom, #ff69b4 0%, #ff1493 100%);
```

Change frosting colors:
- Red: `#ff0000 0%, #dc143c 100%`
- Yellow: `#ffff00 0%, #ffd700 100%`
- Blue: `#0000ff 0%, #00bfff 100%`

## Advanced Customization

### Add Background Music

Add this before the closing `</body>` tag:

```html
<audio autoplay loop>
    <source src="happy-birthday.mp3" type="audio/mpeg">
</audio>
```

### Change Login Title

Find this line (around line 113):
```html
<h1 class="login-title">🎂 Happy Birthday! 🎂</h1>
```

Change to:
```html
<h1 class="login-title">🎂 Happy Birthday, Sarah! 🎂</h1>
```

### Modify Button Text

Find this line (around line 116):
```html
<button class="login-button" onclick="handleLogin()">Unlock Surprise</button>
```

Change to:
```html
<button class="login-button" onclick="handleLogin()">🎁 Open Surprise 🎁</button>
```

### Make It Interactive

Add click handlers to the celebration screen to trigger effects again:

```javascript
document.addEventListener('click', () => {
    if (celebrationContainer.classList.contains('active')) {
        createConfetti();
        createParticles();
    }
});
```

## Tips & Tricks

1. **Test everything** - Make sure to test after each change
2. **Use browser DevTools** - Right-click → Inspect to see live changes
3. **Mobile first** - Test on mobile devices too
4. **Color harmony** - Use https://coolors.co for color schemes
5. **Emoji picker** - Use https://emojipedia.org/ to find emojis
6. **Font awesome icons** - You can also use Font Awesome instead of emojis

## Common Issues

### Image not showing?
- Make sure the image URL is correct
- Check if it's a valid image format (jpg, png, gif)
- Try uploading the image locally

### Passcode not working?
- Check for typos in the CORRECT_PASSCODE variable
- Remember it's case-sensitive
- Make sure you're using quotes: `"1234"` not `1234`

### Message not updating?
- Make sure you're editing the CUSTOM_MESSAGE variable
- Clear browser cache (Ctrl+Shift+Delete)
- Refresh the page (Ctrl+F5)

## Sharing

Once you've customized it:
1. Push changes to GitHub
2. Enable GitHub Pages (Settings → Pages)
3. Share the deployed link with your friend
4. They can visit and see the surprise!

---

Have fun celebrating! 🎉