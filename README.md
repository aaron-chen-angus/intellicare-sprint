# intelliCARE 100m Sprint Game

A polished, embeddable HTML5 mobile-first sprint racing mini-game built for the **intelliCARE Fitness Awards** platform.

## 🎮 Play it live
👉 **https://YOUR-USERNAME.github.io/YOUR-REPO-NAME**
*(Update this link after deploying)*

---

## 📁 Files

| File | Purpose |
|------|---------|
| `index.html` | The complete game — all HTML, CSS, and JS in one file |
| `README.md` | This file |

---

## 🚀 Deploying to GitHub Pages

### Step 1 — Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it e.g. `intellicare-sprint`
4. Set visibility to **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2 — Upload the files
1. On the new repo page, click **Add file → Upload files**
2. Drag and drop both `index.html` and `README.md`
3. Write a commit message e.g. `Add sprint game`
4. Click **Commit changes**

### Step 3 — Enable GitHub Pages
1. Go to the **Settings** tab of your repository
2. In the left sidebar click **Pages**
3. Under **Source**, choose **Deploy from a branch**
4. Set Branch to `main`, folder to `/ (root)`
5. Click **Save**

### Step 4 — Get your live URL
Wait about 60 seconds, then your game is live at:
```
https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPO-NAME/
```
Example: `https://aaronlee.github.io/intellicare-sprint/`

---

## 🔗 Embedding into an existing webpage

**Option A — iframe (simplest, zero style conflict):**
```html
<iframe
  src="https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/"
  width="420"
  height="750"
  style="border:none; border-radius:22px; display:block; margin:auto;"
  allow="autoplay">
</iframe>
```

**Option B — inline paste:**
Copy everything between the two `EMBEDDABLE COMPONENT` comments in `index.html` and paste directly into your target page's `<body>`. All CSS is scoped to `#race-game-container` so it won't affect surrounding styles.

---

## ⚙️ Tuning difficulty

Find the `CFG` block near the top of the `<script>` tag in `index.html`:

```javascript
const CFG = {
  NUM_RUNNERS   : 6,    // Total runners including player
  AI_SPEED_MIN  : 28,   // Slowest AI runner speed
  AI_SPEED_MAX  : 42,   // Fastest AI runner speed
  PLAYER_SPEED  : 15,   // Player base speed without tapping
  TAP_BOOST     : 95,   // Speed burst per tap — raise for easier
  BOOST_DECAY   : 2.8,  // Boost fade rate — raise for harder
  RACE_DISTANCE : 1800, // Race length — raise for longer race
};
```

---

## 📱 Compatibility
- ✅ iOS Safari, Android Chrome — touch input works
- ✅ Desktop Chrome, Firefox, Safari, Edge — mouse click works
- ✅ Portrait-optimised, fluid scaling to any screen width
- ✅ No external libraries or build tools required
