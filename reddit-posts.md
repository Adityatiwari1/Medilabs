# Reddit Posts, Medilab Exports (8 drafts)

Reddit's spam filter is mostly domain-based, not post-based. Same domain linked in 8 posts across 8 subreddits in a short window gets the domain itself auto-filtered site-wide, even if each individual post reads fine. Fix: only 4 of 8 posts below carry a direct link. The other 4 mention the source by name with no URL, you drop the link in a reply if someone asks. That halves domain repetition and looks like organic citation instead of a link campaign.

Also removed all em dashes (auto-mod word lists and some spam classifiers weight em dash + link combos as copy-paste marketing text). Replaced with periods or commas.

---

## 1. r/labrats (no link, no brand mention, rule-blocked)

r/labrats Rule 1 bans ads, promotion, and commercial content outright. This isn't a phrasing problem, any link or brand name here gets removed regardless of how it's worded. Post the value part only, zero Medilab mention, or skip this sub entirely.

**Title:** Class A vs Class B volumetric glassware, what actually changes results?

**Body:**
Had a debate with a coworker over whether Class B volumetric flasks are "good enough" for routine reagent prep vs always defaulting to Class A. Turns out the tolerance gap is bigger than most people assume. A 100 mL Class A flask is plus or minus 0.10 mL, Class B is plus or minus 0.20 mL, and that doubles again at 1000 mL. Doesn't matter for a wash solution. Matters a lot if you're feeding a calibration curve.

Curious what your lab's default is. Class A everywhere, or do you split by application?

---

## 2. r/chemistry (no link)

**Title:** Why does borosilicate 3.3 glass matter so much for lab equipment vs regular glass?

**Body:**
Got asked this by a new grad student and realized my answer was mostly "thermal shock resistance" without really explaining why. Short version: borosilicate 3.3 has a coefficient of thermal expansion around 3.3x10^-6/K vs roughly 9x10^-6/K for soda-lime glass, so it survives rapid heating and cooling and resists most acids, alkalis, and solvents without leaching.

There's a good writeup of the full chemistry on Medilab Exports' blog if anyone wants the deeper version, I'll drop the link below if people want it.

Anyone had a borosilicate flask crack anyway? Usually comes down to point-contact heating or a star crack nobody caught before autoclaving.

---

## 3. r/AskScience (link)

**Title:** What's the actual difference between "To Contain" (TC) and "To Deliver" (TD) markings on glassware?

**Body:**
This trips up a lot of undergrads, mine included. TC and TD look like minor print on the glass but they change how you should read a measurement.

TC (volumetric flasks) means calibrated to hold the stated volume within the glass. TD (pipettes, burettes) means calibrated to deliver that volume when drained, accounting for wetting and drainage residue. Using a TC flask like it's TD, assuming the last adhering drop doesn't count, introduces a real systematic error.

Full explanation with examples: https://medilabexports.com/blog/class-a-vs-class-b-laboratory-glassware

---

## 4. r/microbiology (no link)

**Title:** Glassware vs plasticware for media prep, when does it actually matter?

**Body:**
Following a thread from last week about disposable vs reusable culture vessels. For autoclaved media prep, borosilicate glass still wins on repeated thermal cycling, it won't warp or leach plasticizers, but plasticware is obviously cheaper and lower breakage for high-volume teaching labs.

Saw a decent comparison of cost-per-use, chemical resistance, and where each makes sense (research vs teaching vs industrial QC) on Medilab Exports' site, happy to link it in a reply if useful.

What's your lab standardized on for media bottles specifically?

---

## 5. r/AskAcademia (link)

**Title:** Equipping a new university chemistry lab, glassware checklist for procurement?

**Body:**
Helping a smaller college department scope out their first full glassware order and realized there's no clean single checklist anywhere. Most guides assume you already know what you need.

Found the 10 essentials (beakers through burettes) with typical quantities per bench station laid out here: https://medilabexports.com/blog/top-10-essential-laboratory-equipment-chemistry-labs

If you've done a from-scratch lab buildout, what did you underestimate on the first order? We blew our pipette budget in year one.

---

## 6. r/QualityAssurance (no link)

**Title:** How do you verify a glassware supplier's Class A certification is legit?

**Body:**
Vendor qualification question. We've had suppliers claim ISO 1042 or ASTM E288 compliance without actually providing batch certificates of conformance when asked. What's your team's minimum bar before approving a new glassware vendor for a regulated lab?

Read a good breakdown recently of what a proper certificate should actually contain (standard cited, nominal volume, tolerance class, sampling method) and the red flags to watch for. Can share the source in a reply if anyone wants it.

Anyone here reject a supplier over documentation alone?

---

## 7. r/Pharmacy (link)

**Title:** Why USP/EP assays require Class A glassware specifically, not Class B

**Body:**
Question came up during a QC audit prep. Why does the pharmacopeia insist on Class A for standard solution prep when Class B is "close enough" for most other lab work?

Answer is that Class A tolerance errors don't stay contained to one step. They propagate through every dilution and calculation downstream, and that's exactly what a regulatory inspector will trace back if a result gets challenged. Breakdown with the actual tolerance math: https://medilabexports.com/blog/importance-precision-scientific-glassware

---

## 8. r/india, or r/IndianBusiness / r/ExportImport if allowed, check current self-promo rule before posting (no link)

**Title:** Indian laboratory glassware manufacturers exporting globally, anyone know this space?

**Body:**
Didn't realize until recently how much of the global lab glassware supply (volumetric flasks, pipettes, burettes) is OEM-manufactured out of India and exported under other brands' labels. Makes sense given the borosilicate glass manufacturing base here, but there's surprisingly little written about how the OEM/distributor relationship actually works in this industry.

Found a decent explainer on how the OEM model and distribution works from Medilab Exports Consortium, an Indian manufacturer, can post the link if anyone wants to dig deeper.

Anyone here worked with Indian lab equipment exporters, good or bad experiences?

---

## Why these are less likely to get pulled

- **Domain repetition capped.** Only 4 of 8 posts carry the raw URL. Reddit's spam filter is largely domain-reputation based across the whole site, not per-subreddit, so hammering the same domain 8 times in a short window is what gets a domain shadow-filtered, not any single post's wording.
- **No em dashes, no link-in-title.** Both are common tells auto-mod word lists and spam classifiers weight, especially paired together.
- **Vary posting accounts' behavior, not just text.** Space these days apart, from an account with real comment history in each subreddit already if possible. A brand-new account's first activity being a link post is the single biggest shadowban trigger, bigger than anything in the post text itself.
- **Read each subreddit's self-promo rule before posting, every time.** Many require a 9:1 or 10:1 non-promotional-to-promotional ratio, or a minimum account age and karma before any link post is allowed. r/labrats Rule 1 bans commercial content outright, no phrasing gets around it, that one's marked no-link/no-brand above for that reason.
- **Reddit's own pre-submit checker (the popup you hit on r/labrats) evaluates per-subreddit at submit time.** This list is a starting guess, not a guarantee any of the "(link)" posts clear their sub's checker. If a post gets flagged, don't argue with the popup by rewording, strip the link and brand mention like the r/labrats version above and post the value-only version instead.
- **Reply from the account afterward**, especially on the no-link posts when someone asks for the source. Mods and filters both read a comment-back within hours as real engagement, not drop-and-run.
- **Verify URLs resolve** before posting. These slugs match your existing blog files (blog-02, 03, 04, 09) but confirm they're live on medilabexports.com first, a dead link on a real post is worse than no link.
