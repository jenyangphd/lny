# Lunar New Year — Empire, Migration, and the Bakery Counter

A digital menu + tent card system for a Lunar New Year happy hour.

## How to Publish (GitHub Pages)

### 1. Create a GitHub repository

```bash
# From inside this folder:
git init
git add .
git commit -m "Initial commit: LNY menu site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/lny-menu.git
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under "Source," select **Deploy from a branch**
3. Select **main** branch, **/ (root)** folder
4. Click **Save**
5. Your site will be live at: `https://YOUR-USERNAME.github.io/lny-menu/`

### 3. Update QR codes with your real URL

Before printing tent cards, regenerate QR codes with your actual URL:

1. Open `gen_qr.py` (the generation script, not included in the site)
2. Change `BASE_URL` to your actual GitHub Pages URL
3. Re-run the script
4. Re-run `gen_tent_cards.py` to regenerate tent card PDFs with the new QR codes

### 4. Print tent cards

- Open `assets/tent-cards-all.pdf` (all 7 cards in one file) or individual `tent-card-*.pdf` files
- Print at **100% scale** (do not "fit to page")
- Card size: 4" wide × 6" tall — fold in half to create a tent card
- Recommended paper: 80–100lb cardstock

## File structure

```
lny-menu/
├── index.html                          # Full menu landing page
├── items/
│   ├── fortune-cookies.html
│   ├── pineapple-buns-pandan-kaya.html
│   ├── scallion-salt-bread.html
│   ├── gochujang-caramel-cookies.html
│   ├── hk-milk-tea-cream-puffs.html
│   ├── persimmon-tartlets.html
│   └── du-jjon-ku-strawberries.html
├── assets/
│   ├── qr-*.svg                        # QR codes (SVG)
│   ├── qr-*.png                        # QR codes (PNG)
│   ├── tent-card-*.pdf                 # Individual tent cards
│   └── tent-cards-all.pdf             # All tent cards combined
└── README.md
```
