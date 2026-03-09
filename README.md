# GEO Case Studies: Real-World AI Search Visibility Optimization

As AI-powered search engines like ChatGPT, Perplexity, Google AI Overviews, and Claude reshape how users discover information, **Generative Engine Optimization (GEO)** has become a critical discipline for website owners. But what does GEO look like in practice? How much of a difference do specific optimizations actually make?

This repository collects **real-world case studies** documenting before-and-after improvements in AI search visibility. Each case study walks through the initial state of a website, the specific GEO changes that were implemented, and the measurable results that followed. Whether you run a SaaS platform, an e-commerce store, or a content-driven blog, these examples provide a concrete roadmap for improving how AI systems understand and recommend your content.

All sites were evaluated using [GEOScore AI](https://geoscoreai.com), which scans 11 distinct signals across four categories — Access, Structure, Content, and Authority — and assigns an overall grade from A to F.

---

## Case Study 1: SaaS Documentation Site

**Industry:** B2B SaaS (Developer Tools)
**Site type:** Product documentation and knowledge base (~1,200 pages)
**Initial GEO Grade:** D (38/100)

### Initial State

The documentation site was built with a popular static site generator and had solid traditional SEO. Google ranked it well for branded queries. However, an audit revealed several gaps in AI readiness:

- **robots.txt** blocked several AI crawlers (GPTBot, ClaudeBot, Bytespider) by default, inheriting restrictive rules from an older configuration.
- **No llms.txt file** existed, so AI models had no machine-readable summary of the site's purpose, structure, or key endpoints.
- **Structured data was absent.** Pages had no JSON-LD markup — no `TechArticle`, `HowTo`, or `FAQPage` schemas.
- **Heading hierarchy was inconsistent.** Many pages jumped from `<h1>` directly to `<h4>`, making it harder for AI parsers to extract a logical content outline.

### Changes Made

1. **Updated robots.txt** — Removed blocks for GPTBot, ClaudeBot, PerplexityBot, and other AI crawlers. Added a dedicated AI crawler section with `Allow: /` directives.
2. **Created llms.txt** — Added a structured file at `/llms.txt` describing the product, its documentation sections, API reference entry points, and quickstart guides.
3. **Added JSON-LD structured data** — Implemented `TechArticle` schema on all documentation pages, `HowTo` schema on tutorial pages, and `FAQPage` schema on troubleshooting pages.
4. **Fixed heading hierarchy** — Ensured all pages followed a clean `h1 > h2 > h3` structure.
5. **Added FAQ sections** — Appended a "Common Questions" block to the 50 highest-traffic pages, using `<details>` elements with corresponding `FAQPage` markup.

### Results

| Metric | Before | After (8 weeks) |
|--------|--------|-----------------|
| GEO Grade | D (38/100) | A (91/100) |
| AI Crawler Access Score | 2/10 | 10/10 |
| Structured Data Score | 0/10 | 9/10 |
| llms.txt Present | No | Yes |
| Cited in ChatGPT responses (sampled queries) | 0/20 | 7/20 |
| Perplexity source appearances (monthly) | 12 | 89 |

The most impactful single change was **unblocking AI crawlers** — the site went from being invisible to AI systems to being fully accessible within days.

---

## Case Study 2: E-commerce Product Pages

**Industry:** Consumer Electronics
**Site type:** E-commerce storefront (~3,500 product pages)
**Initial GEO Grade:** D (42/100)

### Initial State

The e-commerce site had strong traditional SEO with rich product listings. However, its AI readiness was poor:

- **robots.txt** used a blanket disallow for all bots except Googlebot, Bingbot, and a few others. AI crawlers were blocked by a catch-all rule.
- **Product schema was incomplete.** While basic `Product` markup existed, it was missing `aggregateRating`, `review`, `brand`, and `offers.availability` properties.
- **No FAQ content.** Product pages had no Q&A sections despite receiving hundreds of pre-purchase questions via customer support.
- **Sitemap was outdated.** The XML sitemap hadn't been regenerated in months and was missing 400+ new product pages.

### Changes Made

1. **Rewrote robots.txt** — Created explicit `Allow` rules for GPTBot, ClaudeBot, PerplexityBot, GoogleOther, and Applebot-Extended. Used the [Robots.txt Generator](https://geoscoreai.com/tools/robots-txt-generator) tool to ensure proper formatting.
2. **Enriched Product schema** — Added `aggregateRating`, `review` (pulling from existing customer reviews), `brand`, `sku`, `gtin`, and `offers.availability` to every product page.
3. **Added FAQ sections** — Mined customer support tickets for the top 5 questions per product category and added `FAQPage` structured data on 200 key product pages.
4. **Regenerated sitemap** — Set up automated daily sitemap regeneration and submitted it to all major search engines and AI crawlers.
5. **Created llms.txt** — Summarized the store's product categories, return policy, shipping info, and top-selling product lines.

### Results

| Metric | Before | After (6 weeks) |
|--------|--------|-----------------|
| GEO Grade | D (42/100) | A (88/100) |
| Product Schema Completeness | 35% | 95% |
| FAQ Coverage (top products) | 0 pages | 200 pages |
| AI Crawler Access | Blocked | Fully allowed |
| Product recommendations in AI answers (sampled) | 1/25 | 9/25 |
| Organic traffic from AI referrals (monthly) | ~200 | ~1,400 |

Adding **rich FAQ content with schema markup** had the most noticeable impact on AI citation rates. AI models frequently pulled answers directly from the FAQ sections.

---

## Case Study 3: Technical Blog

**Industry:** Software Engineering / DevOps
**Site type:** Technical blog (~300 articles)
**Initial GEO Grade:** C (55/100)

### Initial State

The blog already had decent fundamentals — clean HTML, fast load times, and some structured data. But there was room for improvement:

- **No llms.txt** — AI models had no summary file to understand the blog's scope and expertise areas.
- **Article schema was basic.** Only `headline`, `datePublished`, and `author` were present. Missing: `dateModified`, `description`, `wordCount`, `speakable`, and `mainEntityOfPage`.
- **Heading structure was inconsistent.** About 40% of articles used non-hierarchical headings or skipped levels.
- **No explicit AI crawler policies.** The robots.txt neither blocked nor explicitly welcomed AI crawlers.

### Changes Made

1. **Added llms.txt** — Described the blog's focus areas (cloud infrastructure, DevOps, Kubernetes, CI/CD), its most authoritative series, and the author's credentials.
2. **Enhanced Article schema** — Added `dateModified`, `description`, `wordCount`, `speakable` (for key definition paragraphs), `publisher`, and `mainEntityOfPage` to all articles.
3. **Fixed heading hierarchy** — Audited and corrected heading levels across all 300 articles using an automated script.
4. **Added explicit AI crawler access** — Updated robots.txt with explicit `Allow` directives and used the [AI Crawler Checker](https://geoscoreai.com/tools/ai-crawler-checker) to verify accessibility.
5. **Added definition blocks** — For technical terms, added clear one-sentence definitions at the start of relevant sections, improving citation readiness.

### Results

| Metric | Before | After (4 weeks) |
|--------|--------|-----------------|
| GEO Grade | C (55/100) | A (92/100) |
| Structured Data Completeness | 40% | 95% |
| Heading Hierarchy Score | 6/10 | 10/10 |
| AI search citations (sampled weekly) | 3 | 14 |
| Perplexity source appearances (monthly) | 45 | 180 |

The combination of **enhanced Article schema** and **citation-ready definition blocks** drove the largest improvement. AI models increasingly pulled direct quotes from the blog's clearly structured content.

---

## How to Run Your Own GEO Audit

Want to see where your site stands? Run a free scan at **[GEOScore AI](https://geoscoreai.com)**. The tool evaluates all 11 signals across Access, Structure, Content, and Authority and gives you an actionable grade with specific recommendations.

### Free Tools

- **[Robots.txt Generator](https://geoscoreai.com/tools/robots-txt-generator)** — Generate an AI-crawler-friendly robots.txt file in seconds.
- **[AI Crawler Checker](https://geoscoreai.com/tools/ai-crawler-checker)** — Verify whether your site is accessible to major AI crawlers.

---

## Contributing

We welcome community-submitted case studies! If you've improved your site's AI search visibility and have before/after data, please contribute:

1. Fork this repository
2. Create a new file in the `case-studies/` directory using the template below
3. Include before/after GEO grades (from [geoscoreai.com](https://geoscoreai.com))
4. Submit a pull request

### Case Study Template

```markdown
## [Your Site Type / Industry]

**Initial GEO Grade:** [Grade]
**Final GEO Grade:** [Grade]

### Initial State
[Describe the starting conditions]

### Changes Made
[List specific changes]

### Results
[Include metrics table]
```

We review all submissions for quality and accuracy. Approved case studies will be added to this repository and may be featured on the [GEOScore AI blog](https://geoscoreai.com).

---

## Related GEO Resources

### Free Tools
- [GEOScore AI Scanner](https://geoscoreai.com) — Check your website's AI search visibility across 11 signals
- [AI Robots.txt Generator](https://geoscoreai.com/tools/robots-txt-generator) — Generate optimized robots.txt for AI crawlers
- [AI Crawler Access Checker](https://geoscoreai.com/tools/ai-crawler-checker) — Verify which AI bots can access your site

### Open Source Projects
- [awesome-geo](https://github.com/henu-wang/awesome-geo) — Curated list of GEO resources, tools, and guides
- [geo-scoring-methodology](https://github.com/henu-wang/geo-scoring-methodology) — Open methodology for scoring AI search readiness
- [ai-robots-txt-generator](https://github.com/henu-wang/ai-robots-txt-generator) — Generate optimized robots.txt for AI crawlers
- [geo-checklist](https://github.com/henu-wang/geo-checklist) — Interactive pre-launch GEO readiness checklist
- [ai-crawlers-reference](https://github.com/henu-wang/ai-crawlers-reference) — Complete database of AI search engine crawler user-agents
- [geo-badge-generator](https://github.com/henu-wang/geo-badge-generator) — Generate badges showing your GEO readiness score
- [llms-txt-examples](https://github.com/henu-wang/llms-txt-examples) — Real-world llms.txt implementation examples by industry
- [geo-config-examples](https://github.com/henu-wang/geo-config-examples) — Ready-to-use AI search optimization configs for popular frameworks
- [ai-search-readiness-framework](https://github.com/henu-wang/ai-search-readiness-framework) — 11-signal AI search readiness evaluation framework


## License

This repository is licensed under the [MIT License](LICENSE). Case study data is shared with permission from the respective site owners.
