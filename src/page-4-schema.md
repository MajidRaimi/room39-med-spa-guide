# Draft — Page 4: Med Spa Schema Markup: The JSON-LD That Gets You Cited

**Target query:** medical spa schema markup
**Secondary queries:** medical spa schema, med spa schema markup, schema markup for med spa, localbusiness schema med spa, medicalspa schema, healthcare schema med spa, med spa structured data
**Intent:** Informational (action)
**Page type:** Technical how-to
**Cluster:** B — Local and on-page foundations
**Last updated:** 2026-10-26

---

## SEO fields

**Title tag (54 chars):** Med Spa Schema Markup: The JSON-LD That Gets You Cited

**Meta description (142 chars):** Med spas have no schema type of their own. Here is the exact JSON-LD to use instead, the properties Google reads, and the errors that void it.

**Slug:** `/med-spa-schema-markup/`

**Schema:** `Article` + `FAQPage` (the build generates this from the page). The page body also shows a sample `MedicalClinic` JSON-LD inside a fenced code block, because teaching the markup is the point. That sample is article copy and must NOT be emitted as the page's own structured data. Do not add `MedicalBusiness`, `AggregateRating`, or `Review` schema to this page.

**Internal links (build map):**

| Target page | Anchor text | Link |
|---|---|---|
| 1 (live) | how to get your med spa to show up in ChatGPT | `/med-spa-chatgpt-visibility/` |
| 3 (live) | Google Business Profile for med spas | `/google-business-profile-med-spa/` |
| 2 (live) | why Google AI Overviews skip your med spa | `/google-ai-overviews-not-showing-med-spa/` |
| 10 (planned) | local SEO for med spas | `/local-seo-for-med-spas/` |

Forge build notes: add `/med-spa-schema-markup/` to `LIVE_SLUGS` and `INTERNAL_LINKS`, and add the four draft files list entry `page-4-schema.md`. The planned page 10 link unwraps to plain text until that page ships. Offer CTA links use the standard `$99 AI Visibility Snapshot` / `$750 Audit + Fix` label mapping.

---

# Med Spa Schema Markup: The JSON-LD That Gets You Cited

Schema markup tells search engines and AI systems what your med spa is, where it is, and when it is open, in a format they can read without guessing. The catch is that there is no `MedicalSpa` schema type. For a clinic that offers medical treatments, use `MedicalBusiness` or its subtype `MedicalClinic`. For an aesthetics-led spa, use `HealthAndBeautyBusiness` or `DaySpa`. Add the full `LocalBusiness` property set, and put one JSON-LD block on the location's main page.

This guide gives you the exact type, the JSON-LD to paste, and the mistakes that make valid-looking markup worthless.

## What schema markup actually does

Structured data is a standardized format for describing a page. Google's introduction says it uses structured data to understand page content and to gather information about "the people, books, or companies" the markup describes ([Google Search Central, "Introduction to structured data markup in Google Search," accessed 2026-10-26](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)).

The upside is measurable. Google's own case-study list reports that Rotten Tomatoes measured a 25% higher click-through rate on pages with structured data, the Food Network saw a 35% increase in visits after converting pages to enable search features, and Nestlé measured an 82% higher click-through rate on pages that appear as rich results ([Google Search Central, accessed 2026-10-26](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)). Those are vendor-published case studies, so read them as directional.

Schema does not rewrite your content or lift your ranking by itself. It removes ambiguity from facts you already publish: name, address, phone, hours, services, and location.

## There is no "MedicalSpa" schema type

The most common med spa schema mistake is inventing the type. `MedicalSpa` is not in the schema.org vocabulary. Requesting `https://schema.org/MedicalSpa` returns a 404, and the type is absent from the current schema.org release ([schema.org, accessed 2026-10-26](https://schema.org/MedicalSpa)).

When a validator sees `"@type": "MedicalSpa"`, it flags an unrecognized type. You lose the machine-readable meaning you were trying to add, and you gain a review flag.

## Which schema type should a med spa use?

schema.org offers two branches that fit a med spa. Both sit under `LocalBusiness`, so both inherit the address, hours, and location properties.

| Your clinic | Use | Why |
|---|---|---|
| Treatment-led: injectables, lasers, and body treatments under medical direction | `MedicalClinic` | `MedicalClinic` is a subtype of `MedicalBusiness`, which sits under `LocalBusiness` in the health-lifesci extension ([schema.org/MedicalClinic](https://schema.org/MedicalClinic), [schema.org/MedicalBusiness](https://schema.org/MedicalBusiness)). |
| Aesthetics-led: facials, massage, and day-spa services with limited clinical work | `HealthAndBeautyBusiness` or `DaySpa` | `DaySpa` and `BeautySalon` are subtypes of `HealthAndBeautyBusiness`, which is a subtype of `LocalBusiness` ([schema.org/HealthAndBeautyBusiness](https://schema.org/HealthAndBeautyBusiness), [schema.org/DaySpa](https://schema.org/DaySpa)). |

If the clinic offers medical treatments under a licensed provider, `MedicalClinic` is the safer primary type. Use `HealthAndBeautyBusiness` only when the business genuinely is a spa. Do not emit both types on the same node to hedge. Pick the one that describes the core business, then let the service list carry the rest.

### One entity per location

Each physical location gets its own page and its own JSON-LD block with a stable `@id`. Two clinics means two blocks, each on its own location page. Duplicate blocks are the second most common error after the invented type, and they split the entity signals Google is trying to assemble.

## The med spa JSON-LD to paste

Here is a complete example for a single-location clinic. Replace every placeholder with your real details, and keep the structure.

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalClinic",
  "@id": "https://www.example.com/locations/scottsdale/#clinic",
  "name": "Glow Aesthetics Scottsdale",
  "description": "Independent medical spa offering injectables, laser treatments, and skin care in Scottsdale, Arizona.",
  "url": "https://www.example.com/locations/scottsdale/",
  "telephone": "+1-480-555-0142",
  "image": "https://www.example.com/images/glow-aesthetics-scottsdale.jpg",
  "priceRange": "$$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "4820 N Scottsdale Rd, Suite 210",
    "addressLocality": "Scottsdale",
    "addressRegion": "AZ",
    "postalCode": "85251",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 33.4942,
    "longitude": -111.9261
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "09:00",
      "closes": "17:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Saturday",
      "opens": "10:00",
      "closes": "14:00"
    }
  ],
  "areaServed": {
    "@type": "City",
    "name": "Scottsdale"
  },
  "sameAs": [
    "https://www.google.com/maps/place/example",
    "https://www.instagram.com/example"
  ]
}
```

### The properties that matter most

| Property | What it does | Common mistake |
|---|---|---|
| `@type` | Names the business | Using `MedicalSpa`, which does not exist |
| `@id` | Gives the entity a permanent identifier | Omitting it, then repeating the block on other pages |
| `name` | States the real-world business name | Adding city or treatment keywords |
| `address` | Gives the postal address as a `PostalAddress` object | Splitting the address into free-text fields |
| `geo` | Gives latitude and longitude | Pin dropped on a nearby plaza, not the door |
| `telephone` | Gives the primary phone number | A tracking number that changes over time |
| `openingHoursSpecification` | Gives hours by day | Hours when the phone is not answered |
| `url` | Points at the location page | Pointing every location at the homepage |
| `sameAs` | Lists the profiles you control (Google Business Profile, social) | Linking profiles you do not own |
| `areaServed` | Names the city or region you serve | Listing a metro you cannot actually serve |

`sameAs` is how you connect the site to the profiles you already maintain. Add your Google Business Profile URL and your social profiles, and nothing else. Every URL should resolve to a page you control.

## What not to put in med spa schema

Google's structured data policies are a hard gate. Markup that violates them can trigger a manual action, and a structured data manual action removes rich result eligibility for the page ([Google Search Central, "Structured data general guidelines," accessed 2026-10-26](https://developers.google.com/search/docs/appearance/structured-data/sd-policies)).

- **Reviews you did not collect.** Do not add `aggregateRating` or `review` properties for reviews that are not on the page or are not genuine. Faking them breaks the policy and, in most markets, advertising law.
- **Content a reader cannot see.** Do not mark up a service, price, or provider the page does not show. Google's guidelines require the markup to be a true representation of the visible page.
- **Clinical claims.** Do not describe treatment outcomes, efficacy, or safety in schema. This is marketing markup, not a medical claim.
- **Invented types.** Stay inside the schema.org vocabulary. Unrecognized types are ignored.
- **A `@type` you cannot support.** If you are not a `MedicalClinic`, do not label yourself one to chase a category.

## How to add and validate the markup

1. Put the JSON-LD in the `<head>` of the location page, inside a `<script type="application/ld+json">` block.
2. Validate the structure in the [Schema Markup Validator](https://validator.schema.org/).
3. Run the page through Google's [Rich Results Test](https://search.google.com/test/rich-results) to see what Google parses.
4. After deployment, check the live URL in Search Console's URL Inspection tool.
5. Keep the markup in sync with your Google Business Profile. Change hours in one place, change them in both.

FAQ and HowTo markup are a separate story. In August 2023 Google limited FAQ rich results to well-known, authoritative government and health sites, and in September 2023 it retired HowTo rich results entirely ([Google Search Central, "Changes to HowTo and FAQ rich results," published 2023-08-08, updated 2023-09-14](https://developers.google.com/search/blog/2023/08/howto-faq-changes)). Those blocks can still clarify entities for machines, but do not build a content plan around a rich result you will not get.

## Does schema markup help AI search?

Partly. Google states there are "no additional requirements to appear in AI Overviews or AI Mode" and that "there's also no special schema.org structured data that you need to add" ([Google Search Central, "AI features and your website," accessed 2026-10-26](https://developers.google.com/search/docs/appearance/ai-features)). The same page says to make sure "your structured data matches the visible text on the page."

Schema is a foundation, not a lever. The research on generative engines points at content signals instead. A KDD 2024 study found that optimization tactics such as adding citations, quotations, and statistics can lift a page's visibility in generative engine responses by up to 40% ([Aggarwal et al., "GEO: Generative Engine Optimization," arXiv:2311.09735, KDD 2024](https://arxiv.org/abs/2311.09735)).

The practical order is this: make the facts machine-readable with schema, then make the page worth citing with sourced, specific content.

## Frequently asked questions

### Is there a MedicalSpa schema type?

No. `MedicalSpa` is not part of the schema.org vocabulary and returns a 404 on schema.org. Use `MedicalClinic` or `MedicalBusiness` for a treatment-led clinic, or `HealthAndBeautyBusiness` or `DaySpa` for an aesthetics-led spa.

### Should a med spa use MedicalBusiness or LocalBusiness?

`MedicalBusiness` is already a `LocalBusiness` subtype, so use `MedicalBusiness` or `MedicalClinic` and you inherit the full `LocalBusiness` property set. You do not need to emit `LocalBusiness` as a second type.

### Does schema markup improve Google rankings?

Not directly. Google uses structured data to understand a page and to power rich results. The benefit comes from clearer entity signals and a higher click-through rate, not from the markup itself.

### Can I add my Google reviews with schema?

Only if those reviews are visible on the page and genuinely collected. Google prohibits marking up reviews that misrepresent the page, and a business's own review snippets about itself are not eligible for review rich results.

### Does FAQ schema still show rich results?

For most med spas, no. Since August 2023 Google shows FAQ rich results only for well-known, authoritative government and health websites. Keep an `FAQPage` block for entity clarity if you want, but do not expect a rich result.

### Do I need schema on every page?

No. Put the `MedicalClinic` or `HealthAndBeautyBusiness` block on the location page it describes. Supporting articles can carry `Article` markup. One entity, one page.

### How do I check my med spa schema?

Run the URL through the Schema Markup Validator and Google's Rich Results Test, then check the live page in Search Console's URL Inspection tool.

## What to do next

Add the `MedicalClinic` or `HealthAndBeautyBusiness` block to your location page this week, validate it, and align it with your Google Business Profile. That gives every other page a clean entity to link back to.

If the profile is not finished, start with [Google Business Profile for med spas](/google-business-profile-med-spa/). For the wider strategy, read [how to get your med spa to show up in ChatGPT](/med-spa-chatgpt-visibility/) and [why Google AI Overviews skip your med spa](/google-ai-overviews-not-showing-med-spa/). When you cover more than one city, do it without doorway pages in [local SEO for med spas](/local-seo-for-med-spas/).

Our [$99 AI Visibility Snapshot](/ROO/issues/ROO-4) checks whether ChatGPT, Google AI Overviews, and Perplexity name your clinic for your top five treatments and shows where the facts disagree. The [$750 Audit + Fix](/ROO/issues/ROO-4) covers the schema, profile, and on-page work.

**Keep reading:**
- [How to Get Your Med Spa to Show Up in ChatGPT](/med-spa-chatgpt-visibility/) — the hub guide
- [Google Business Profile for Med Spas](/google-business-profile-med-spa/) — the 12-point checklist
- [Why Google AI Overviews Skip Your Med Spa](/google-ai-overviews-not-showing-med-spa/) — the three reasons and their fixes
- [Local SEO for Med Spas Without Doorway Pages](/local-seo-for-med-spas/) — the compliant way to cover a metro

---

## Sources (accessed 2026-10-26)

1. schema.org. "MedicalBusiness." https://schema.org/MedicalBusiness — definition; subclass of LocalBusiness; part of the health-lifesci extension.
2. schema.org. "MedicalClinic." https://schema.org/MedicalClinic — subclass of MedicalBusiness and MedicalOrganization.
3. schema.org. "HealthAndBeautyBusiness." https://schema.org/HealthAndBeautyBusiness — subclass of LocalBusiness.
4. schema.org. "DaySpa." https://schema.org/DaySpa — subclass of HealthAndBeautyBusiness.
5. schema.org. "MedicalSpa." https://schema.org/MedicalSpa — returns 404; the type does not exist in the vocabulary.
6. Google Search Central. "Introduction to structured data markup in Google Search." https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data — what structured data is; JSON-LD; case studies: Rotten Tomatoes 25% higher CTR, Food Network 35% increase in visits, Nestlé 82% higher CTR.
7. Google Search Central. "Structured data general guidelines." https://developers.google.com/search/docs/appearance/structured-data/sd-policies — markup must be a true representation of the visible page; manual action risk; no invisible content.
8. Google Search Central. "Changes to HowTo and FAQ rich results." Published 2023-08-08, updated 2023-09-14. https://developers.google.com/search/blog/2023/08/howto-faq-changes — FAQ rich results limited to well-known, authoritative government and health sites; HowTo rich results deprecated 2023-09-13.
9. Google Search Central. "AI features and your website." https://developers.google.com/search/docs/appearance/ai-features — no additional requirements for AI Overviews or AI Mode; no special schema.org structured data required; structured data should match visible text.
10. Aggarwal, P., Murahari, V., Rajpurohit, T., Kalyan, A., Narasimhan, K., Deshpande, A. "GEO: Generative Engine Optimization." arXiv:2311.09735, KDD 2024. https://arxiv.org/abs/2311.09735 — GEO can boost visibility in generative engine responses by up to 40%; tactics include citing sources, quotations, and statistics.

**Verification note:** All primary sources were fetched and read on 2026-10-26. The schema.org hierarchy and the `MedicalSpa` 404 were verified against the current schema.org release JSON. The page makes no medical or treatment-outcome claims. No reviews, testimonials, or patient data are invented.
