# Parascand Notary — Website

A complete, SEO-optimized static website for Parascand Notary. Drop the folder on any host (Netlify, Vercel, GoDaddy, Bluehost, GitHub Pages, S3) and it works — no build step.

## What's in here

```
website/
├── index.html              Homepage
├── medical-notary.html     Medical/bedside notary specialty (lead SEO page)
├── services.html           Full service menu with section anchors
├── service-areas.html      Richmond, NoVA, Charlottesville coverage
├── about.html              About James Parascand & credentials
├── contact.html            Contact form + info card
├── faq.html                Comprehensive FAQ (rich-result eligible)
├── styles.css              Shared design system (navy + gold, serif headings)
├── sitemap.xml             For Google Search Console
├── robots.txt              Crawl directives
└── images/
    ├── README.txt          Where to drop your headshot
    └── headshot.jpg        ← save your headshot here
```

## Before you launch — required

1. **Save your headshot** at `images/headshot.jpg` (the same image you sent in chat). The site references it on the homepage hero and About page; it falls back gracefully if missing, but the site looks far better with it.
2. **Buy the domain** `parascandnotary.business` (or whatever you prefer) and update the `<link rel="canonical">` and `og:url` tags throughout if you choose a different domain.
3. **Verify the contact info** on every page — phone (571) 332-3829 and email parascandconsulting@gmail.com appear in the header, footer, hero, contact card, and schema.org JSON-LD.

## SEO baked in

- **Schema.org JSON-LD** on every page (LocalBusiness, ProfessionalService, Service, FAQPage, BreadcrumbList, Person)
- **Open Graph + Twitter cards** for social sharing previews
- **Canonical URLs** to avoid duplicate-content penalties
- **Semantic HTML5** with proper H1 → H2 → H3 hierarchy
- **Sitemap.xml + robots.txt** ready for Google Search Console submission
- **Mobile-responsive** with sticky call button at the bottom
- **Click-to-call tel: links** on every page
- **Local SEO keywords** woven through copy: Richmond, NoVA, Charlottesville, hospital notary, bedside notary, mobile notary Virginia, etc.
- **FAQ rich-result schema** — eligible to appear as expandable answers in Google search results
- **Fast load** — no JS frameworks, just one tiny CSS file and Google Fonts

## After launch — do these in week 1

1. **Submit to Google Search Console** at search.google.com/search-console
   - Add property → enter your domain → verify (usually via DNS TXT record)
   - Submit `https://yourdomain.com/sitemap.xml`
2. **Submit to Bing Webmaster Tools** at bing.com/webmasters (covers Bing + DuckDuckGo)
3. **Create / claim Google Business Profile** at google.com/business — single biggest local-SEO lever
4. **Add the website URL** to every listing in your Game Plan: Snapdocs, NotaryDash, Yelp, Thumbtack, Nextdoor, NNA, NotaryRotary, etc.
5. **Get reviews** — Google Business Profile reviews are the single biggest organic ranking factor for local notary search. Ask every client.

## After launch — do these in month 1

- Replace placeholder testimonials in `index.html` (lines starting around line 290) with real client quotes
- Add `images/og-image.jpg` (1200×630px) for prettier social sharing — currently referenced but not present
- Set up form handling — `contact.html` currently uses `mailto:`. For a real form backend that won't trigger spam filters, use Formspree (free), Basin, or Web3Forms. Replace the form's `action="mailto:..."` with the service's endpoint URL.
- Add Google Analytics 4 or Plausible to track which pages convert to calls
- Consider adding a **blog** at `/blog/` with posts like "What to bring to a hospital notary appointment" or "Virginia healthcare power of attorney explained" — content like this ranks well for medical-notary searches

## Visual style

- **Primary:** Deep navy `#0A2540` (trust, legal weight)
- **Accent:** Warm gold `#C9A961` (premium, established)
- **Headings:** Cormorant Garamond (serif, professional)
- **Body:** Inter (clean, readable)

To tweak any of these, edit `:root` at the top of `styles.css`.

## Hosting recommendations

- **Netlify** (free tier): drag-and-drop the folder, custom domain, automatic HTTPS. Easiest path.
- **Vercel** (free tier): same idea, drag-and-drop or git deploy.
- **GoDaddy / Bluehost / namecheap shared hosting**: upload via FTP. Works fine.
- **Cloudflare Pages**: free, fast, custom domain.

All four give you free HTTPS, which Google requires for ranking.

---

Need changes? Common edits:
- **Phone number**: search-and-replace `(571) 332-3829` and `+15713323829` across all `.html` files
- **Email**: search-and-replace `parascandconsulting@gmail.com`
- **Domain**: search-and-replace `parascandnotary.business` (canonical URLs, schema, OG tags, sitemap)
- **Brand colors**: edit `:root` variables at the top of `styles.css`
