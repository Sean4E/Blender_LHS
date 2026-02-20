# LHS Blender Proposal — GitHub Pages Setup

## Files in this folder

```
index.html       ← Landing page + password gate
proposal.html    ← Full proposal (auth-protected)
LHS.png          ← Lighthouse Studios logo  (add this)
4e.png           ← 4E Virtual Design logo   (add this)
Blender_Icon.png ← Blender logo             (optional)
README.md        ← This file
```

---

## Setup Steps

### 1. Create a GitHub account
Go to https://github.com and sign up (free).

### 2. Create a new repository
- Click **New repository**
- Name it something like `lhs-proposal` (this becomes part of the URL)
- Set to **Public** (required for free GitHub Pages)
- Click **Create repository**

### 3. Upload the files
- Click **Add file → Upload files**
- Drag in: `index.html`, `proposal.html`, `LHS.png`, `4e.png`
- Click **Commit changes**

### 4. Enable GitHub Pages
- Go to **Settings → Pages**
- Source: **Deploy from a branch**
- Branch: `main` / Folder: `/ (root)`
- Click **Save**

### 5. Your live URL
After ~60 seconds the site is live at:

```
https://YOUR-USERNAME.github.io/lhs-proposal/
```

Send that URL to LHS. Access code: **LHS1**

---

## Notes

- Password is never stored in plain text — SHA-256 hashed in source.
- `sessionStorage` holds the auth token, clears when the tab closes.
- Direct navigation to `proposal.html` redirects back to the gate.
- To change the password: generate a new SHA-256 hash at
  https://emn178.github.io/online-tools/sha256.html
  and replace the HASH value in both `index.html` and `proposal.html`.
