# Draft — Page 2: Why Google AI Overviews Skip Your Med Spa

**Target query:** google ai overviews not showing my business
**Secondary queries:** ai overviews not showing, why is my business not in ai overviews, google ai overview not appearing, ai overviews local business
**Intent:** Informational (awareness)
**Page type:** Explainer
**Cluster:** A — AI search visibility
**Last updated:** 2026-10-12

---

## SEO fields

**Title tag (56 chars):** Google AI Overviews Not Showing Your Med Spa? Here's Why

**Meta description (141 chars):** AI Overviews skip most med spas for one of three reasons. Here is how to tell which one is yours, and the exact fix for each, in plain steps.

**Slug:** `/google-ai-overviews-not-showing-med-spa/`

**Schema:** `Article` + `FAQPage`. Author `Person` with the Room 39 byline. Do not add `MedicalBusiness`, `Product`, or `Review` schema to this page.

**Internal links (build map):**

| Target page | Anchor text | Link |
|---|---|---|
| 1 (live) | how to get your med spa to show up in ChatGPT | `/med-spa-chatgpt-visibility/` |
| 3 (planned) | Google Business Profile for med spas | `/google-business-profile-med-spa/` |
| 4 (planned) | med spa schema markup | `/med-spa-schema-markup/` |
| 8 (planned) | audit your AI visibility in 30 minutes | `/ai-visibility-audit/` |
| 6 (live) | AI visibility tracking tools | `/best-ai-visibility-tools-med-spa/` |

Unpublished targets use planned slugs above; Forge maps them at build time, same as the first batch.

---

# Why Google AI Overviews Skip Your Med Spa

AI Overviews skip your med spa for one of three reasons. The overview may not trigger for that query at all, your page may not be eligible because it is not indexed or not snippet-eligible, or your page is eligible but not chosen as a supporting link. Each reason has a different fix, and guessing wrong wastes months.

This page shows you how to tell the three apart, what Google actually requires, and the med spa mistakes that keep a clinic out of the answer.

## What an AI Overview is, and why it often never appears

An AI Overview is a generated summary at the top of some Google results, built from pages in Google's search index, with links to the sources it used. Google states that AI Overviews "are only shown when our systems determine that it is additive to classic Search, and as such, often don't trigger" ([Google Search Central, updated 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).

That single sentence explains most of what med spa owners report. An empty overview is not always a penalty or a bug. It often means Google decided that query did not need one.

Overviews are also becoming more common. Pew Research found that 18% of the Google searches in its March 2025 sample produced an AI summary, and that 88% of those summaries cited three or more sources ([Pew Research Center, 2025-07-22](https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/)).

The practical takeaway: before you try to fix your clinic's absence, confirm an overview even appears for the query you care about.

## The three reasons, and how to tell them apart

| What you see | Most likely reason | First thing to check |
|---|---|---|
| No AI Overview for anyone, even your competitors | The query does not trigger an overview | Run the query in a clean, signed-out browser |
| An AI Overview appears, but it never names your clinic | You are eligible but not selected | Who is cited, and where your page ranks |
| Your page cannot be used at all | You are not eligible: not indexed or snippet-blocked | Search Console URL Inspection |

Work down that list in order. Each row has a different fix, and most wasted effort comes from treating a selection problem as an eligibility problem, or the other way around.

## Reason 1: The query does not trigger an AI Overview

Google says AI Overviews help people "get to the gist of a complicated topic or question more quickly," and it triggers them where generative AI adds something beyond the usual results ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).

That means short, local, navigational queries often get a map pack and a Business Profile instead of an overview. Longer questions that compare, explain, or ask for a number are the ones more likely to trigger one:

- "how much does Botox cost in [city]"
- "med spa vs dermatologist for [treatment]"
- "how long does [treatment] last"

Test this yourself. Open an incognito window, set your location, and search the exact query. Then search a competitor's city and a close variant. If no overview appears for anyone, there is nothing to be missing from. Move your effort to a query that actually triggers one.

If the overview does appear, and your competitor is in it, go to Reason 3.

## Reason 2: Your page is not eligible

Google is specific about eligibility. To be shown as a supporting link in AI Overviews or AI Mode, a page "must be indexed and eligible to be shown in Google Search with a snippet, fulfilling the Search technical requirements." It also states plainly: "There are no additional technical requirements" ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).

In the same guide, Google says you do not need new machine-readable files, AI text files, or special schema markup to appear in these features. If an agency sold you an `llms.txt` file as the fix for AI Overviews, that is not what Google documents.

So eligibility is the boring checklist. Run it on the one page you most want cited:

- **Indexed?** Check the URL in Search Console's URL Inspection tool. "Discovered" or "Crawled — currently not indexed" means the page is not in play.
- **Snippet allowed?** Look for `noindex`, `nosnippet`, `data-nosnippet`, or a low `max-snippet` in the page template, the CMS SEO plugin, or the page itself. An old agency or a security plugin can leave these behind.
- **Canonical correct?** If the canonical tag points at a different URL, Google is indexing that URL instead of the one you are watching.
- **Crawlable?** Confirm `robots.txt`, your CDN, or your hosting layer is not blocking Googlebot.
- **Textual content present?** Google's guidance is to make important content available in textual form. If your treatment details only load after a click, they may not count as page content ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).
- **Business Profile complete?** Google says businesses with complete and accurate information "are more likely to show up in local search results," and that inaccurate info can keep a profile from appearing for relevant local searches ([Google Business Profile Help](https://support.google.com/business/answer/7091)). Verify the profile and finish every field, including categories and hours.

One clarification worth keeping straight: Google-Extended controls AI training and grounding in some of Google's other systems, not whether your page can appear as a link in AI Overviews. Googlebot directives are the control for Search. Do not confuse the two when you audit.

## Reason 3: You are eligible but not selected

Google builds each overview from a limited set of supporting links. Meeting the eligibility bar does not guarantee one of them. As Google puts it: "Just because a page meets all requirements, best practices, and complies with the policies, doesn't mean that Google will crawl, index, or serve its content. Indexing and serving isn't guaranteed" ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).

Selection follows Google's core ranking and quality systems, which is why general SEO still applies. The strongest signals for a clinic:

1. **A clear, liftable answer.** Models pull passages. Put a self-contained answer in the first 40 to 60 words under a heading, naming the treatment, the city, and the detail.
2. **Pages that match real questions.** One strong page per core treatment and location beats a "services" page. AI-native queries average around 23 words, versus roughly four for traditional search ([Andreessen Horowitz, 2025-05-28](https://a16z.com/geo-over-seo/)), so the phrasing people use is specific.
3. **Entity consistency.** The same business name, address, phone, and hours across your site, your Business Profile, Yelp, and other directories. Contradictions lower confidence.
4. **Third-party confirmation.** Reviews, local media, and complete directory and provider profiles act as outside evidence. This is earned, not faked.
5. **Sources and real numbers.** The GEO research paper found optimization can lift visibility in generative engines, and that citing sources and adding statistics were among the strongest tactics, while keyword stuffing moved visibility the wrong way ([Aggarwal et al., KDD 2024](https://arxiv.org/abs/2311.09735)).
6. **Structured data that matches the page.** Schema does not unlock AI Overviews by itself, but Google says structured data should match the visible text on the page, so keep it accurate ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)).

## The six med spa mistakes that keep a clinic out

1. **An unverified or half-finished Business Profile.** Google explicitly ties completeness to local visibility.
2. **One "our services" page for everything.** No page answers "[treatment] in [city]," so there is nothing to cite.
3. **Inconsistent facts.** Different phone numbers, suite numbers, or hours across listings.
4. **Accidental blocking.** `noindex` or a crawler block inherited from a past agency or plugin.
5. **No extractable answer.** A padded intro that never states the price, the treatment, or the city in a quotable sentence.
6. **Thin reviews and citations.** No review flow and empty directory profiles, so the model has little outside confirmation.

None of these are exotic. They are the same foundations that help you rank, which is Google's point: optimizing for AI features is optimizing for search.

## How to diagnose your own clinic in 30 minutes

1. **Confirm the overview exists.** Search the query in a clean, signed-out browser with your location set. If there is no overview for anyone, pick a query that has one.
2. **Inspect the page.** Run your money page through Search Console's URL Inspection. Write down indexed status, canonical, and any snippet controls.
3. **Note who is cited.** Record the clinics and sites named in the overview, and where your page ranks below them.
4. **Check the Business Profile.** Confirm verification, categories, hours, address, and services are complete.
5. **Compare your facts.** List your name, address, phone, and hours from your site, your profile, and your top two directories. Fix every mismatch.
6. **Score the page against the six selection signals above.** Circle the weakest one and fix that first.

This is the same walkthrough behind our free [AI visibility audit](/ROO/issues/ROO-4), and it is the method behind the [$99 AI Visibility Snapshot](/ROO/issues/ROO-4).

## What actually moves the needle

- Fix eligibility before selection. There is no point optimizing a page Google cannot index or use.
- Make the answer liftable. One plain sentence per heading that names the treatment, city, and detail.
- Get the entity facts identical everywhere.
- Build one strong treatment-and-city page instead of ten thin ones.
- Earn reviews and complete your directory profiles.
- Re-check monthly, because overviews change with the model and the index.

## Frequently asked questions

### Why do AI Overviews show for my competitor but not my clinic?

That is usually a selection problem, not a technical one. Your page may be eligible while your competitor's page is clearer, better ranked, better confirmed by reviews and directories, or simply more specific to the query. Compare the two pages on the six signals above before changing code.

### Why did my Google traffic drop when AI Overviews appeared?

Pew Research found that users clicked a traditional search result in 8% of visits with an AI summary, versus 15% without one ([Pew Research Center, 2025-07-22](https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/)). Some clicks move into the summary itself. The response is not to fight the overview but to become one of the sources it names, so you keep the brand exposure and the higher-intent clicks that follow.

### Do I need llms.txt or special schema to appear in AI Overviews?

No. Google says you do not need new machine-readable files, AI text files, or special schema markup to appear in AI Overviews, and that the usual foundational SEO practices apply ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)). Keep your structured data accurate and matching the visible page, and spend the rest of the effort on content and eligibility.

### Do AI Overviews hurt local businesses?

They change where the click happens. Google says clicks from pages with AI Overviews tend to be higher quality, meaning people stay longer once they arrive ([Google Search Central, 2025-12-10](https://developers.google.com/search/docs/appearance/ai-features)). For a clinic, the goal shifts from owning every click to being the name and the source the answer uses.

### How long until my med spa appears in AI Overviews?

There is no fixed clock. Google re-crawls on its own schedule, and selection depends on ranking, the query, and your competition. Fix eligibility first, then improve the page and its supporting signals, and re-run the same diagnostic monthly so you can see movement.

## What to do next

Start with the 30-minute diagnostic. Eligibility problems are free to fix and they block everything else.

If you would rather have someone run it, our [$99 AI Visibility Snapshot](/ROO/issues/ROO-4) checks whether ChatGPT, Google AI Overviews, and Perplexity name your clinic for your top five treatments, and shows exactly where you are missing. Our [$750 Audit + Fix](/ROO/issues/ROO-4) handles the technical and on-page work once you are ready.

**Keep reading:**
- [How to Get Your Med Spa to Show Up in ChatGPT](/ROO/issues/ROO-4) — the hub guide
- [Google Business Profile for Med Spas](/ROO/issues/ROO-4) — the 12-point checklist
- [Med Spa Schema Markup](/ROO/issues/ROO-4) — the JSON-LD that gets you cited
- [How to Audit Your Med Spa's AI Visibility in 30 Minutes](/ROO/issues/ROO-4) — the full walkthrough

---

## Sources (accessed 2026-10-12)

1. Google Search Central. "AI features and your website." https://developers.google.com/search/docs/appearance/ai-features — eligibility requirements, trigger behavior, no special files or schema required, structured data should match visible text, Search Console measurement. Last updated 2025-12-10.
2. Pew Research Center. "Google users are less likely to click on links when an AI summary appears in the results." Athena Chapekis and Anna Lieb, 2025-07-22. https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/ — 18% of sampled searches produced an AI summary; 8% click rate with a summary versus 15% without; 88% of summaries cited three or more sources.
3. Google Business Profile Help. "Tips to improve your local ranking on Google." https://support.google.com/business/answer/7091 — verify the business, complete and accurate info, reviews, photos.
4. Andreessen Horowitz. "How Generative Engine Optimization (GEO) Rewrites the Rules of Search." Zach Cohen and Seema Amble, 2025-05-28. https://a16z.com/geo-over-seo/ — AI-native queries average about 23 words.
5. Aggarwal, P., et al. "GEO: Generative Engine Optimization." arXiv:2311.09735, KDD 2024. https://arxiv.org/abs/2311.09735 — optimization can lift generative-engine visibility; citing sources and statistics are strong tactics; keyword stuffing hurts.
6. Google Search Central. "Optimizing your website for generative AI features on Google Search." https://developers.google.com/search/docs/fundamentals/ai-optimization-guide — generative AI features are rooted in core Search ranking and quality systems; query fan-out.

**Verification note:** All primary sources were fetched and read on 2026-10-12. No medical or treatment-outcome claims are made on this page. No invented reviews, testimonials, or patient data.

