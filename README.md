# byteflow-ai-labs-website

# 📸 How to Add Images & Videos to Your ByteFlow Website

## 🎯 Quick Start Guide

### Method 1: Store Files in GitHub (Recommended for Small Files)

#### Step 1: Create Folders
In your GitHub repository, create these folders:
```
byteflow-website/
├── images/
│   ├── logo.png
│   ├── team-photo.jpg
│   ├── hero-bg.jpg
│   └── client-logos/
└── videos/
    └── intro.mp4
```

#### Step 2: Upload Files
1. Go to your GitHub repository
2. Click "Add file" → "Upload files"
3. Drag images/videos into the upload area
4. Commit changes

#### Step 3: Use in HTML
```html
<!-- For Images -->
<img src="images/logo.png" alt="Logo">
<img src="images/team-photo.jpg" alt="Team Photo">

<!-- For Background Images -->
<div style="background-image: url('images/hero-bg.jpg');">
  <!-- Content here -->
</div>
```

---

## Method 2: Use External Hosting (Recommended for Large Files)

### For Images - Use Imgur (FREE)

1. Go to https://imgur.com
2. Click "New post"
3. Upload your image
4. Right-click image → "Copy image address"
5. Use in HTML:
```html
<img src="https://i.imgur.com/YOUR_IMAGE_ID.jpg" alt="Description">
```

### For Videos - Use YouTube (FREE & Best Performance)

1. Upload video to YouTube
2. Click "Share" → "Embed"
3. Copy the iframe code
4. Paste in your HTML:

```html
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
    <iframe 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
        src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
    </iframe>
</div>
```

---

## 📋 Common Use Cases

### 1. Add Logo to Header
Replace emoji with your logo:

```html
<div class="logo">
    <a href="index.html">
        <img src="images/logo.png" alt="ByteFlow Logo" style="height: 40px; vertical-align: middle;"> 
        ByteFlow AI Labs
    </a>
</div>
```

### 2. Add Hero Background Image
```html
<section class="hero" style="background: linear-gradient(rgba(26,115,232,0.8), rgba(13,71,161,0.8)), url('images/hero-bg.jpg') center/cover no-repeat;">
    <h1>Welcome to ByteFlow AI Labs</h1>
</section>
```

### 3. Add Team Photos
```html
<div class="team-image">
    <img src="images/team-photo.jpg" alt="Our Team" style="max-width: 100%; border-radius: 10px;">
</div>
```

### 4. Add Client Logos
```html
<div class="client-card">
    <img src="images/client-logos/techstart.png" alt="TechStart Inc" style="width: 100px; margin-bottom: 20px;">
    <h3>TechStart Inc</h3>
    <p>Client testimonial here...</p>
</div>
```

### 5. Add Demo Video (YouTube)
```html
<section class="section">
    <h2 class="section-title">See Our Platform in Action</h2>
    <div style="max-width: 800px; margin: 0 auto;">
        <div style="position: relative; padding-bottom: 56.25%; height: 0;">
            <iframe 
                style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
                src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
                allowfullscreen>
            </iframe>
        </div>
    </div>
</section>
```

### 6. Add Video from Your Server (Small Files Only)
```html
<video controls style="max-width: 100%; border-radius: 10px;">
    <source src="videos/intro.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
```

---

## 🎨 Image Optimization Tips

### Before Uploading:
1. **Resize images** to actual display size (e.g., 1920px width for hero images)
2. **Compress images**: Use https://tinypng.com (FREE)
3. **Use correct formats**:
   - Photos: `.jpg` (smaller file size)
   - Logos/Icons: `.png` (transparent background)
   - Modern sites: `.webp` (best compression)

### Recommended Sizes:
- Logo: 200px × 80px
- Hero background: 1920px × 1080px
- Team photos: 800px × 600px
- Profile photos: 300px × 300px
- Icons: 128px × 128px

---

## 📦 File Size Limits

### GitHub Repository:
- ✅ Single file: Up to 100MB
- ✅ Repository: Up to 1GB total
- ⚠️ Keep images under 5MB each
- ⚠️ Videos: Use YouTube instead

### Vercel Deployment:
- ✅ Total size: Up to 100MB (free plan)
- 💡 For larger files, use external hosting

---

## 🔥 Best Practices

1. **Always use descriptive alt text** for accessibility
```html
<img src="images/team.jpg" alt="ByteFlow AI Labs team meeting in 2024">
```

2. **Use responsive images**
```html
<img src="images/hero.jpg" 
     style="max-width: 100%; height: auto;" 
     alt="Description">
```

3. **Lazy load images** (for faster page load)
```html
<img src="images/large-photo.jpg" loading="lazy" alt="Description">
```

4. **Optimize for mobile**
```css
@media (max-width: 768px) {
    img {
        max-width: 100%;
        height: auto;
    }
}
```

---

## 🆓 Free Image Resources

### Stock Photos (Commercial Use):
- Unsplash: https://unsplash.com
- Pexels: https://pexels.com
- Pixabay: https://pixabay.com

### Icons:
- Font Awesome: https://fontawesome.com
- Flaticon: https://flaticon.com
- Icons8: https://icons8.com

### Image Editing:
- Canva: https://canva.com (FREE)
- Photopea: https://photopea.com (FREE Photoshop alternative)
- Remove.bg: https://remove.bg (Remove backgrounds)

---

## 🚀 Quick Example: Full Homepage with Images

```html
<section class="hero" style="background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?w=1920') center/cover;">
    <img src="images/logo.png" alt="ByteFlow Logo" style="width: 150px; margin-bottom: 30px;">
    <h1>Welcome to ByteFlow AI Labs</h1>
    
    <!-- Demo Video -->
    <div style="max-width: 700px; margin: 30px auto;">
        <iframe 
            width="100%" 
            height="400"
            src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
            frameborder="0"
            allowfullscreen>
        </iframe>
    </div>
</section>
```

---

## 💡 Need Help?

If you get stuck:
1. Check that file paths are correct
2. Make sure images are uploaded to GitHub
3. Test in browser developer tools (F12)
4. Verify image URLs are accessible

**Your images should work immediately after pushing to GitHub and Vercel auto-deploys!**

---

## 📝 Checklist Before Deployment

- [ ] All images compressed (under 1MB each)
- [ ] All images have descriptive alt text
- [ ] Videos hosted on YouTube (not in repo)
- [ ] File paths are correct (case-sensitive!)
- [ ] Images look good on mobile
- [ ] Logo is high resolution
- [ ] Background images are 1920px wide

**You're ready to deploy! 🚀**