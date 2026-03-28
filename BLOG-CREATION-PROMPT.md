# Master Blog Creation Prompt — Medilab Exports SEO Blog Series

Use this prompt every time a new blog topic is assigned. Read it fully before writing anything.

---

## CONTEXT: WHO WE ARE

**Company:** Medilab Exports Consortium
**Product:** ISO-certified borosilicate 3.3 laboratory glassware (Class A and Class B)
**Markets served:** 40+ countries — pharmaceutical labs, university research, clinical diagnostics, hospital central stores, laboratory equipment distributors
**Key credentials:** ISO 9001, ISO 17025, WHO-GMP, CE marking, ISO 4787 batch documentation
**Manufacturing heritage:** 60+ years in borosilicate 3.3 glassware
**Target reader:** Laboratory managers, procurement managers, scientific equipment distributors, lab technicians, researchers

**Tone:** Professional, B2B, evidence-based. No marketing fluff. No em dashes (use hyphens or restructure). Short paragraphs (2-4 sentences max).

---

## DELIVERABLES FOR EVERY BLOG TOPIC

Create exactly **4 items** per topic:

1. `blog-[XX]-wordpress.md` — WordPress body content (paste into WP Editor > Text/HTML view)
2. `blog-[XX]-seo-doc.md` — Full SEO documentation
3. `blog-[XX]-[permalink-slug].html` — Standalone HTML file
4. Update `index.html` — Add new blog card + increment article counter

---

## PART 1: FOCUS KEYWORD AND TITLE RULES

### Focus Keyword Selection
- Choose a keyword with clear commercial or informational intent matching the topic
- 3-5 words preferred (e.g., `laboratory glassware breakage`, `Indian lab equipment manufacturers`)
- Must be naturally repeatable throughout the content

### Title Formula (ALL four elements required)
```
[Focus Keyword]: [Number] [Power Word] [Topic Expansion] [Positive/Negative Sentiment Word]
```
- Focus keyword must appear at the very START of the title
- Include a number (7, 9, 12, 15, etc.)
- Power word examples: Proven, Essential, Critical, Complete, Definitive
- Sentiment word examples: Prevent, Master, Need, Avoid, Every Lab
- Keep under 100 characters total
- Example: "Laboratory Glassware Breakage: 9 Common Causes and Proven Prevention Strategies"

### Permalink
- Lowercase hyphenated slug of the focus keyword
- No stop words, no numbers
- Example: `laboratory-glassware-breakage`

---

## PART 2: WORDPRESS MD FILE — STRUCTURE AND FORMAT

Follow this exact structure. Reference: blog-10-wordpress.md, blog-13-wordpress.md, blog-14-wordpress.md.

### File Header Block (not pasted into WP — metadata only)
```
# Blog [XX] – WordPress Body Content (Paste into WP Editor > Text/HTML View)

**Title:** [Full SEO title]
**Focus Keyword:** [focus keyword]
**Permalink:** [slug]
**Category:** [category]
**Tags:** [comma-separated tags]

---
```

### Body Content Order

**1. Three intro `<p>` paragraphs — NO wrapper div**
- Para 1: Establish the problem/opportunity + first use of focus keyword in sentence 1
- Para 2: What this guide covers + second use of focus keyword
- Para 3: Medilab Exports authority paragraph + third use of focus keyword
- Each paragraph is 3-4 sentences. Short. Direct.

**2. Featured image — `<figure>` tag format**
```html
<figure class="wp-block-image">
<img src="https://medilabexports.com/wp-content/uploads/2026/03/[filename].jpg" alt="[focus keyword] - [descriptive context]" title="[Full blog title]" width="800" height="450" loading="lazy" />
<figcaption>[Descriptive caption using focus keyword]</figcaption>
</figure>
```

**3. Table of Contents — styled `<nav>` block**
```html
<nav class="lab-toc" style="background:#f0f7ff;border-left:4px solid #0073aa;padding:20px 24px;border-radius:4px;margin:24px 0;">
<h2 style="margin-top:0;">Table of Contents</h2>
<ol>
<li><a href="#section-id">Section Title</a></li>
...
</ol>
</nav>
```

**4. H2 sections with IDs**
- Use `<h2 id="section-id">Section Title</h2>`
- One intro H2 before the numbered sections (e.g., "Why X Matters", "The Rise of X")
- Then numbered or reason-based H2 sections (7-9 main sections is ideal)
- Each section: 2-3 `<p>` paragraphs + optional `<ul>` list for scannability
- Include focus keyword at least once per section naturally

**5. Second inline figure image (place after section 4 or 5)**
- Same format as featured image above
- Different image description and alt text (still includes focus keyword)

**6. Comparison or reference `<table>`**
- Must include a table summarizing key content (causes vs prevention, comparison of options, priority reference, etc.)
- Minimum 4 columns, 5+ rows
- Introduce table with a `<p>` that uses the focus keyword

**7. "How to" or summary section with internal links**
- 3-4 paragraphs
- Must include exactly 3 internal links to existing blogs
- Format: `<a href="blog-07-common-laboratory-glassware-uses.html">anchor text</a>`

**8. FAQ section — CSS + JS accordion design**

Use this EXACT format (copy every class name and style):
```html
<h2 id="faq">Frequently Asked Questions</h2>

<style>
.faq-item { border: 1px solid #dde3ec; border-radius: 6px; margin-bottom: 10px; overflow: hidden; }
.faq-question { background: #f4f8fc; padding: 16px 20px; cursor: pointer; display: flex; justify-content: space-between; align-items: center; font-weight: 600; font-size: 16px; color: #1a2e4a; user-select: none; }
.faq-question:hover { background: #e6f0fa; }
.faq-question::after { content: '+'; font-size: 22px; font-weight: 400; color: #0073aa; flex-shrink: 0; margin-left: 12px; transition: transform 0.3s; }
.faq-item.open .faq-question::after { content: '-'; }
.faq-answer { max-height: 0; overflow: hidden; transition: max-height 0.35s ease, padding 0.35s ease; padding: 0 20px; background: #fff; }
.faq-item.open .faq-answer { max-height: 600px; padding: 16px 20px; }
</style>

<div class="faq-wrapper">
<div class="faq-item">
<div class="faq-question">Question text here?</div>
<div class="faq-answer"><p>Answer text here. Use <strong>focus keyword</strong> naturally in answer.</p></div>
</div>
... repeat for each question ...
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  var faqItems = document.querySelectorAll('.faq-item');
  faqItems.forEach(function(item) {
    var question = item.querySelector('.faq-question');
    question.addEventListener('click', function() {
      var isOpen = item.classList.contains('open');
      faqItems.forEach(function(i) { i.classList.remove('open'); });
      if (!isOpen) { item.classList.add('open'); }
    });
  });
});
</script>
```
- Write 6-7 FAQ questions
- Use focus keyword in at least 4 answers
- Each answer is 3-5 sentences. Short paragraphs.

**9. CTA box — inline styled, after FAQ**
```html
<div class="cta-box" style="background:#f0f7ff;border:2px solid #0073aa;padding:24px;border-radius:8px;text-align:center;margin-top:32px;">
<h3 style="margin-top:0;">[CTA Headline related to blog topic]</h3>
<p>[2-3 sentences describing what Medilab offers, using focus keyword once]</p>
<a href="https://medilabexports.com/contact" style="background:#0073aa;color:#fff;padding:14px 32px;border-radius:5px;text-decoration:none;font-weight:bold;display:inline-block;margin-top:10px;" target="_blank" rel="noopener noreferrer">[Button Text]</a>
</div>
```
- CTA button text options: "Request a Product Catalog", "Request Distributor Pricing", "Request a Quote", "Contact Our Team"

---

## PART 3: KEYWORD DENSITY RULES

- **Target: ~1% density = 25-35 occurrences in ~3,000-3,500 words**
- Count using the full focus keyword phrase (exact match preferred, natural variations acceptable)
- Keyword must appear in:
  - [ ] Title (first position)
  - [ ] First sentence of para 1
  - [ ] Paras 2 and 3 (once each)
  - [ ] At least one H2 heading
  - [ ] Featured image alt text
  - [ ] Inline image alt text
  - [ ] Every major H2 section body (at least once per section)
  - [ ] Table intro paragraph
  - [ ] "How to" summary section (2-3 times)
  - [ ] At least 4 FAQ answers
  - [ ] CTA body text
- **Never force** the keyword unnaturally. If a paragraph resists it, skip rather than stuff.
- Use `<strong>` tags on the focus keyword for the first 3-4 occurrences in the body, then sparingly

---

## PART 4: LINKS

### Internal Links (exactly 3 per blog)
Always link to these blogs where relevant:
- `blog-07-common-laboratory-glassware-uses.html` — glassware types and uses
- `blog-08-importance-precision-scientific-glassware.html` — precision in scientific glassware
- `blog-12-laboratory-glassware-quality-standards.html` — ISO/ASTM/DIN quality standards
- Other blog links are acceptable when highly relevant

### External DoFollow Links (minimum 2 per blog)
Use authoritative sources relevant to the topic:
- ISO standards: `https://www.iso.org/standard/[standard-number].html`
- WHO GMP guidelines
- Make in India: `https://www.makeinindia.com/`
- ASTM standards
- Format: `<a href="[URL]" target="_blank" rel="noopener noreferrer">anchor text</a>`

---

## PART 5: WRITING RULES

- **No em dashes** anywhere. Use hyphens or restructure sentences.
- **Short paragraphs** — 2-4 sentences maximum per paragraph
- **Bullet lists** for prevention steps, specification parameters, and checklist-style content
- **Active voice** preferred
- **No filler phrases**: "It is worth noting that...", "In conclusion...", "As mentioned above..."
- **No hedging language**: "might", "could potentially", "it seems"
- **Bold `<strong>`** only on focus keyword (first few occurrences) and table headers
- Word count target: **3,000-3,500 words** for the wordpress.md body

---

## PART 6: IMAGES

Every blog needs exactly **2 images**, both as `<figure>` tags.

For each image provide:
- Detailed visual description (what the photographer/designer should create)
- Alt text: `[focus keyword] - [specific visual description of what's in the image]`
- Title: matches the blog title or a relevant variation
- Suggested file name: `[focus-keyword-slug]-[descriptor].jpg`
- Width: 800px, Height: 450px for inline; 1200x630px for featured

---

## PART 7: SEO DOC FILE STRUCTURE

The seo-doc.md file must contain these 11 sections:

1. **Focus Keyword** — primary + secondary keywords
2. **SEO Title** — with character count and title checklist
3. **Permalink / URL** — full URL + checklist
4. **Meta Description** — under 160 chars + trimmed version
5. **On-Page SEO Checklist** — keyword placement, content quality, links
6. **Internal Linking Map** — table of anchor text, target page, relevance
7. **External DoFollow Links** — table of anchor, URL, context
8. **Image Specifications** — both images with full description, alt text, file name
9. **JSON-LD Structured Data** — complete BlogPosting schema code block
10. **Content Summary** — table with focus keyword, title, permalink, word count, audience, funnel stage, CTA, date
11. **Sections Covered** — numbered list of all H2 sections with brief description of content

---

## PART 8: HTML STANDALONE FILE STRUCTURE

The `.html` file follows a **4-row layout** using the existing `lab-glassware-blogs.css` stylesheet.

### Head section:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>[Blog Title] | Medilab Exports</title>
  <meta name="description" content="[Meta description under 160 chars]" />
  <meta name="keywords" content="[focus keyword, secondary keywords]" />
  <meta name="author" content="Medilab Exports Consortium" />
  <link rel="canonical" href="https://medilabexports.com/blog/[permalink]" />
  <meta property="og:title" content="[Blog Title]" />
  <meta property="og:description" content="[Meta description]" />
  <meta property="og:type" content="article" />
  <meta property="og:url" content="https://medilabexports.com/blog/[permalink]" />
  <link rel="stylesheet" href="lab-glassware-blogs.css" />
  <script type="application/ld+json">
  { [JSON-LD BlogPosting schema] }
  </script>
</head>
```

### Body structure:
```
<article class="blog-post">
  <a href="index.html" class="back-link">← Back to Index</a>

  <!-- ROW 1: HEADER -->
  <div class="row row--header">
    <span class="article-badge">Article [X] of 16</span>
    <h1 class="blog-title">[Title]</h1>
    <div class="image-placeholder featured"> [image spec block] </div>
    <div class="introduction"> [3 intro paragraphs] </div>
    <nav class="toc"> [TOC ol list] </nav>
  </div>

  <!-- ROW 2: BODY CONTENT -->
  <div class="row row--body">
    [H2 sections with class="section-heading"]
    [inline image-placeholder div in middle of sections]
    [table]
    [summary section with internal links]
  </div>

  <!-- ROW 3: FAQ -->
  <div class="row row--faq">
    <h2 class="section-heading" id="faq">Frequently Asked Questions</h2>
    [<details><summary>Question</summary><p>Answer</p></details> — one per FAQ]
  </div>

  <!-- ROW 4: CTA -->
  <div class="row row--cta">
    <div class="cta-box">
      <h2 class="cta-heading">[CTA headline]</h2>
      <p class="cta-sub">[CTA body]</p>
      <a href="https://medilabexports.com/contact" class="cta-btn" ...>[Button text]</a>
    </div>
  </div>
</article>
```

**Important:** HTML standalone files use `<details>`/`<summary>` for FAQ, NOT the JS accordion. The JS accordion is only for the wordpress.md file.

### Image placeholders in HTML files:
```html
<div class="image-placeholder featured">
  <div class="img-header">📷 FEATURED IMAGE</div>
  <div class="img-grid">
    <div class="img-field full"><label>Description</label><span>[detailed description]</span></div>
    <div class="img-field"><label>Alt Text</label><span>[alt text]</span></div>
    <div class="img-field"><label>Suggested Size</label><span>1200 × 630 px</span></div>
    <div class="img-field"><label>File Name</label><span>[filename.jpg]</span></div>
  </div>
</div>
```

---

## PART 9: INDEX.HTML UPDATE RULES

After creating the 3 blog files, update `index.html`:

1. Add a new `<a class="blog-card">` after the last existing blog card
2. Increment the hero counter: `<span>📄 [N] Blog Articles</span>`

### Blog card format:
```html
<a class="blog-card" href="blog-[XX]-[slug].html">
  <div class="card-header">
    <span class="article-number">Blog [XX]</span>
    <span class="card-icon">[relevant emoji]</span>
    <h2>[Full blog title]</h2>
  </div>
  <div class="card-body">
    <p>[1-2 sentence description of what the blog covers]</p>
    <div class="card-tags">
      <span class="tag">[Tag 1]</span><span class="tag">[Tag 2]</span><span class="tag">[Tag 3]</span>
    </div>
    <span class="read-btn">Read Article <span class="arrow">→</span></span>
  </div>
</a>
```

---

## PART 10: PRE-PUBLISH QUALITY CHECKLIST

Before finishing, verify:

### SEO
- [ ] Focus keyword in first sentence of the blog
- [ ] Focus keyword in title (first word/phrase)
- [ ] Focus keyword in permalink
- [ ] Meta description under 160 characters and contains focus keyword
- [ ] 25-35 keyword occurrences in body content
- [ ] No paragraph longer than 4 sentences
- [ ] No em dashes in any file
- [ ] 2 external DoFollow links
- [ ] 3 internal links to existing blogs
- [ ] 2 figure image tags with keyword in alt text
- [ ] Styled TOC present
- [ ] Table present (comparison, reference, or summary)
- [ ] 6-7 FAQ questions

### WordPress MD
- [ ] No `<html>`, `<head>`, or `<body>` tags
- [ ] FAQ uses CSS + JS accordion (`.faq-item` / `.faq-question` / `.faq-answer`)
- [ ] CTA uses inline `style=""` attributes
- [ ] Images use `<figure class="wp-block-image">` format

### HTML File
- [ ] Article badge shows correct number (e.g., "Article 15 of 16")
- [ ] FAQ uses `<details>`/`<summary>` (NOT JS accordion)
- [ ] `<link rel="stylesheet" href="lab-glassware-blogs.css" />` present
- [ ] JSON-LD script tag in `<head>` with correct permalink in `mainEntityOfPage`
- [ ] Canonical URL matches permalink
- [ ] Back link to index.html present

### Index.html
- [ ] New blog card added after last existing card
- [ ] Article counter incremented by 1

---

## REFERENCE: EXISTING BLOGS

| Blog # | Topic | Focus Keyword | Slug |
|---|---|---|---|
| 01 | What is laboratory glassware? | laboratory glassware | what-is-laboratory-glassware |
| 02 | Types of laboratory glassware | types of laboratory glassware | types-of-laboratory-glassware |
| 03 | Borosilicate glass properties | borosilicate glass | borosilicate-glass-properties |
| 04 | Laboratory glassware cleaning | laboratory glassware cleaning | laboratory-glassware-cleaning |
| 05 | Lab glassware safety | lab glassware safety | lab-glassware-safety |
| 06 | Laboratory glassware sterilization | laboratory glassware sterilization | laboratory-glassware-sterilization |
| 07 | Common laboratory glassware uses | common laboratory glassware | common-laboratory-glassware-uses |
| 08 | Precision scientific glassware | precision scientific glassware | importance-precision-scientific-glassware |
| 09 | Laboratory glassware suppliers | laboratory glassware suppliers | laboratory-glassware-suppliers |
| 10 | Volumetric flask uses | volumetric flask uses | volumetric-flask-uses-types |
| 11 | Laboratory glassware manufacturing | laboratory glassware manufacturing | laboratory-glassware-manufacturing-process |
| 12 | Laboratory glassware quality standards | laboratory glassware quality standards | laboratory-glassware-quality-standards |
| 13 | Laboratory equipment for biology labs | laboratory equipment for biology labs | laboratory-equipment-for-biology-labs |
| 14 | Indian lab equipment manufacturers | Indian lab equipment manufacturers | indian-lab-equipment-manufacturers |
| 15 | Laboratory glassware breakage | laboratory glassware breakage | laboratory-glassware-breakage |

---

## EXAMPLE INVOCATION

When a topic is given, respond with:

> "Creating Blog [XX]: [Topic]
> Focus keyword: [keyword]
> Title: [full title]
> Permalink: [slug]
> Writing 3 files + updating index.html..."

Then create all 4 deliverables in order: wordpress.md → seo-doc.md → [slug].html → index.html update.
