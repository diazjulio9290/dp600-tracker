# DP-600 · 30-Day Expedition 🧭

A self-contained, hands-on study tracker for the **Microsoft DP-600 (Fabric Analytics Engineer Associate)** exam. One HTML file. No build step, no dependencies, no backend.

- ✅ 30-day plan mapped to the real exam blueprint (Prepare Data 45–50%, Semantic Models 25–30%, Maintain 25–30%)
- ✅ Daily concept + metaphor + Microsoft Learn resource + hands-on task
- ✅ Progress auto-saves in your browser (`localStorage`)
- ✅ Export / Import your progress as JSON to move between devices

---

## Option A — Deploy via the GitHub website (no terminal)

1. Go to **github.com → New repository**. Name it `dp600-tracker`, set it **Public**, create it.
2. Click **Add file → Upload files**, drag in `index.html` (and optionally this `README.md`), commit.
3. Go to **Settings → Pages**.
4. Under *Build and deployment → Source*, pick **Deploy from a branch**, branch **`main`**, folder **`/ (root)`**, **Save**.
5. Wait ~1 minute, then refresh. Your live URL appears at the top:
   `https://<your-username>.github.io/dp600-tracker/`

Bookmark that URL on your phone and laptop. Done.

---

## Option B — Deploy via git (terminal)

```bash
# from inside this folder
git init
git add index.html README.md
git commit -m "DP-600 30-day study tracker"
git branch -M main
git remote add origin https://github.com/<your-username>/dp600-tracker.git
git push -u origin main
```

Then enable Pages: **Settings → Pages → Deploy from a branch → main → /(root) → Save.**

---

## How progress is saved

Progress is stored in your **browser's localStorage**, so it persists per-browser/per-device automatically — no login, nothing leaves your machine.

To carry progress to another device:
1. Click **⤓ Export progress** → saves `dp600-progress.json`.
2. On the other device, open the same site → **⤒ Import progress** → pick that file.

Want a permanent versioned record? Commit `dp600-progress.json` into the repo whenever you export it. Your study history becomes part of your git log — fitting, given Day 22 is literally about Git integration. 😏

---

## Note on "keep track of my work" across devices

localStorage is **per-browser**, so checking off a day on your laptop won't auto-appear on your phone. The Export/Import buttons bridge that gap manually. If you later want true real-time sync across devices, the clean upgrade is a tiny free backend (e.g. a Firebase Firestore doc) — ask and it's a ~20-line swap of the two storage functions.
