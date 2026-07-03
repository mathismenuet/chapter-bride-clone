# Chapter Bride Clone — Milla Nova

**A complete, offline-ready static clone of [chapter.millanova.com](https://chapter.millanova.com)** — the cinematographic wedding collection showcase site.

[![Live on Vercel](https://img.shields.io/badge/live-chapter--bride--clone.vercel.app-blue?style=flat-square)](https://chapter-bride-clone.vercel.app)

---

## 🎯 Overview

This is a **100% static Nuxt 3 SSG (Static Site Generation)** clone of the original Milla Nova "Chapter Bride" site. It features:

- **WebGL 3D effects** (Three.js + GSAP) with interactive card carousel
- **4 wedding themes** (Eat Marry Love, La Storia, Wine O'Clock, Amour Getaway) with prerendered routes
- **HD videos** (4 × ~7–10 MB intro films) with poster images and dynamic 3D textures
- **Smooth scroll & custom cursor** (Lenis + Gsap)
- **Fully local offline mode** — no external dependencies (fonts, GTM, analytics)
- **Responsive design** (mobile, tablet, desktop)

---

## 📦 What's Inside

```
├── index.html                           # Homepage (entry point)
├── eat-marry-love/index.html            # Theme 1 page
├── la-storia/index.html                 # Theme 2 page
├── wine-o-clock/index.html              # Theme 3 page
├── amour-getaway/index.html             # Theme 4 page
├── _nuxt/                               # Compiled Nuxt bundle (all assets inline)
│   ├── DFxf35Yj.js                      # Main bundle (Three.js, GSAP, Nuxt runtime)
│   ├── entry.DxcKQp9o.css               # Tailwind CSS
│   ├── *.woff                           # Local fonts (Bague, Movie)
│   └── noise.CQZxDjFQ.png               # Film grain texture
├── fonts/                               # Google Fonts (localized)
│   ├── fonts.css                        # Font-face definitions
│   └── *.woff2                          # Italiana, Monoton, Over the Rainbow
├── images/                              # Static assets
│   ├── logo.png, favicon.ico
│   ├── txt-1..4.png                     # Title overlays
│   ├── p1..4.svg                        # 3D card posters (SVG)
│   └── poster-1..4.jpg                  # Card textures (JPG)
├── video/                               # HD intro films
│   ├── eat-intro.mp4 / .jpg
│   ├── la-intro.mp4 / .jpg
│   ├── wine-intro.mp4 / .jpg
│   └── amour-intro.mp4 / .jpg
└── vercel.json                          # Vercel static site config
```

**Total size:** ~110 MB (mostly videos)  
**Bundle:** ~830 KB (Three.js + GSAP inlined, everything compressed)

---

## 🚀 Deployment

### Live Instance
- **Production:** [chapter-bride-clone.vercel.app](https://chapter-bride-clone.vercel.app)
- **GitHub Repo:** [github.com/mathismenuet/chapter-bride-clone](https://github.com/mathismenuet/chapter-bride-clone)
- **Vercel Dashboard:** [vercel.com/.../chapter-bride-clone](https://vercel.com)

### Local Development

**Option 1: With the Launch Script (macOS)**
```bash
# Double-click "Lancer le site.command" in the parent folder
# (or run from Terminal)
cd "path/to/chapter-bride-clone"
bash "../Lancer le site.command"
```
Opens http://localhost:8787 in your browser. Ctrl-C to stop.

**Option 2: Manual**
```bash
cd chapter-bride-clone
python3 -m http.server 8787
# Then open http://localhost:8787
```

---

## ✨ Features

### WebGL 3D Rendering
- Interactive Three.js scene with real-time camera control
- 4 dynamic 3D card objects with photo/SVG textures
- GSAP-powered animations (tweens, scroll triggers, morphing)
- Film grain overlay + light/shadow depth effects

### Video Integration
- Muted video backgrounds (autoplay ready)
- Poster images for fallback rendering
- Dynamic playback on theme card interaction

### Fonts & Typography
- **Display fonts** (Italiana, Monoton, Over the Rainbow) — locally hosted
- **Body font** (Bague) — inlined in bundle
- **Film credits font** (Movie) — inlined in bundle
- Google Fonts replaced with local `.woff2` files (offline mode)

### Offline Mode
- ✅ **No external dependencies**  
- ✅ **Google Tag Manager neutralized** (GTM host redirected to dead domain)
- ✅ **All fonts local**  
- ✅ **All assets in repo**  
- ✅ **Works fully offline** once downloaded

---

## 🔧 Technical Details

### Built With
- **Nuxt 3** (Static Site Generation / SSG)
- **Vue 3** (framework)
- **Three.js** (WebGL 3D)
- **GSAP 3** (animations)
- **Tailwind CSS v3** (utility styling)
- **Lenis** (smooth scrolling)

### Browser Support
- Chrome/Edge 120+
- Firefox 120+
- Safari 15+
- Mobile (iOS Safari, Chrome Mobile)

### Performance
- **First Contentful Paint:** ~1.2s (local server), ~2.5s (Vercel)
- **Largest Contentful Paint:** ~4–6s (4 videos loading)
- **Core Web Vitals:** Good (local), Fair (videos on slow connections)

### Known Limitations
- **Audio:** Videos are muted by default (browsers require user interaction for autoplay with sound)
- **3D Performance:** Software rendering on headless/CI environments
- **Mobile:** Touch gestures for camera control (mouse drag on desktop)

---

## 🔍 Verification Checklist

✅ **All assets present & served locally**  
✅ **4 theme routes prerendered** (eat-marry-love, la-storia, wine-o-clock, amour-getaway)  
✅ **Bundle patched** (GTM disabled, googletagmanager.com → gtm.disabled.invalid)  
✅ **Fonts localized** (5 × woff2 files)  
✅ **Videos included** (4 × ~7–10 MB HD films)  
✅ **3D textures complete** (4 × SVG + 4 × JPG card images)  
✅ **Homepage + 4 subpages** working  
✅ **Vercel deployment** live and passing  

---

## 📝 Notes

### Cloning Process
This site was cloned from https://chapter.millanova.com using a combination of:
1. Static HTML export (Nuxt SSG)
2. Manual asset discovery (videos, fonts, 3D textures)
3. Bundle patching (GTM/analytics removal for offline mode)
4. Route completion (prerendered theme pages)

### Future Improvements
- [ ] Optimize video delivery (streaming/adaptive bitrate)
- [ ] Add audio toggle for theme intros
- [ ] Dark mode variant
- [ ] Internationalization (i18n)
- [ ] WebP image format fallbacks

---

## 📄 License

This is a **clone/mirror** for educational & archival purposes. Original design & content are property of [Milla Nova](https://millanova.com). 

Cloning & rehosting done with attribution. For commercial use, contact Milla Nova directly.

---

## 🤝 Contributing

Found a bug or missing asset?
1. Fork the repo
2. Create a branch: `git checkout -b fix/issue-name`
3. Commit: `git commit -m "Fix: description"`
4. Push: `git push origin fix/issue-name`
5. Open a Pull Request

---

**Made with ❤️ for wedding design inspiration**  
Deployed live on Vercel • Hosted on GitHub
