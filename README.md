# CoinWisdom — SEO Affiliate Website

A complete static coin collecting & price guide website monetized with eBay Partner Network affiliate links.

## Files

```
coin-site/
├── index.html                        ← Homepage
├── articles/
│   ├── morgan-dollar-value.html      ← 1921 Morgan Dollar guide (~1,100 words)
│   ├── wheat-penny-guide.html        ← Wheat penny price guide (~1,150 words)
│   ├── silver-quarters.html          ← Silver quarters guide (~1,050 words)
│   ├── error-coins.html              ← Error coins guide (~1,200 words)
│   └── coin-grading.html             ← Grading guide (~1,050 words)
├── sitemap.xml                       ← For Google indexing
├── robots.txt                        ← Standard SEO setup
└── README.md                         ← This file
```

**Total estimated word count: ~5,600 words across 5 articles**

## Monetization

All articles include eBay affiliate link placeholders using this format:
```
https://www.ebay.com/sch/i.html?_nkw=KEYWORD&mkcid=1&mkrid=711-53200-19255-0&siteid=0&campid=CAMPAIGN_ID&customid=TRACKING&toolid=10001&mkevt=1
```

### To activate affiliate links:
1. Sign up at https://partnernetwork.ebay.com/
2. Get your Campaign ID (replace `CAMPAIGN_ID` in all HTML files)
3. Find & replace `CAMPAIGN_ID` across all files:
   ```bash
   find . -name "*.html" -exec sed -i 's/CAMPAIGN_ID/YOUR_ACTUAL_ID/g' {} \;
   ```

## Deployment: GitHub Pages (Free)

### Step 1: Create GitHub Account
- Go to https://github.com and create a free account

### Step 2: Create a Repository
- Click "New repository"
- Name it: `coinwisdom` (or any name)
- Set to **Public**
- Click "Create repository"

### Step 3: Upload Files
**Option A: GitHub web interface**
1. Drag & drop all files into the repository
2. Click "Commit changes"

**Option B: Git command line**
```bash
cd /path/to/coin-site
git init
git add .
git commit -m "Initial CoinWisdom site"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/coinwisdom.git
git push -u origin main
```

### Step 4: Enable GitHub Pages
1. Go to repository Settings → Pages
2. Source: Deploy from branch
3. Branch: `main` / `/ (root)`
4. Click Save
5. Your site will be live at: `https://YOURUSERNAME.github.io/coinwisdom/`

### Step 5: Update Sitemap & robots.txt
Replace `YOURDOMAIN.github.io/coin-site` in `sitemap.xml` and `robots.txt` with your actual URL.

### Step 6: Submit to Google
1. Go to https://search.google.com/search-console
2. Add your site as a property
3. Submit the sitemap URL

## Custom Domain (Optional)
- Buy a domain from Namecheap or Google Domains (~$12/year)
- In GitHub Pages settings, add your custom domain
- Add a CNAME DNS record pointing to `YOURUSERNAME.github.io`

## SEO Tips
- Add 2-3 new articles per month on coin-related topics
- Internal link between articles
- Target keywords: "[coin name] value", "[coin name] worth", "rare [coin type]"
- Submit individual article URLs to Google Search Console after publishing

## Revenue Potential
- eBay Partner Network pays ~50-70% of eBay's commission (typically $1-5 per sale)
- Focus on high-value items (Morgan dollars, graded coins) for better commissions
- 1,000 monthly visitors → estimated $50-200/month
- 10,000 monthly visitors → estimated $500-2,000/month
- SEO takes 3-12 months to gain traction — be patient
