# SpiceX Bright (design contract, Nov 2026)

## Brand overview
SpiceX sells six seasoning blends (Daily Blend, Taco Blast, Sweet Sriracha, Golden Hive, Bella Blend, Oh' Cajun) direct to home cooks, co-founded by creator Karim Saad. The site should feel bright, friendly, flavor-first, and a little funny. Direction set by the owner: the energy of a subscription-first breakfast brand (playful, colorful, box-building), applied to seasoning. The SpiceX logo and jar labels do not change.

## Design thesis
Every blend owns a color, the page is mostly white and warm cream, and one flame-orange button tells you where to tap.

## Colors
| Name | Value | Token | Role |
| --- | --- | --- | --- |
| Ink | #16120E | --s2-ink | Text, dark band |
| Muted | #5B544C | --s2-muted | Secondary text |
| White | #FFFFFF | --s2-white | Page |
| Cream | #FFF4E3 | --s2-cream | Tinted panels, footer |
| Sand | #FBEBD2 | --s2-sand | Image wells, tracks |
| Flame | #D23C14 | --s2-flame | Primary buttons, stat band (white text passes 4.5:1) |
| Flame dark | #B5310E | --s2-flame-dk | Hover, small accent text |
| Gold | #F7B32B | --s2-gold | Stars, step numbers, announcement bar (ink text only) |
| Line | #EADFCB | --s2-line | Hairlines |
Blend colors (tile fill / text): Daily #4D5057 white, Taco #D4302C white, Sweet Sriracha #F47A3F ink, Golden Hive #F7B32B ink, Bella #2F6B34 white, Oh' Cajun #8C2F26 white. Product pages use a pale tint of the blend color as the hero background.

## Typography
- Display: Gabarito 700 to 900 (Google Fonts, loaded in layout/theme.liquid), fallback 'Trebuchet MS', 'Segoe UI', system-ui. Sentence case. Line height 0.96 to 1.1, letter spacing -0.02em to -0.035em.
- Body: DM Sans 400 to 700, 15 to 18px, line height 1.45 to 1.5, letter spacing 0.
- No serif, no all caps headings. Small caps labels only for stat labels.

## Spacing and composition
Section padding 56px. Page gutters 14 to 20px on mobile. Cards and media radius 22px (--s2-r). Buttons are pills. Max content width 1180 to 1220px. Shadows only under jar renders.

## Components
- Primary button (.s2-btn): flame pill, white 17px Gabarito 700, 52px tall.
- Text link (.s2-link): ink, 2px underline.
- Flavor tile (.s2-flavor): blend color fill, jar render, name, descriptor, price, white Add pill.
- Starter pack (.s2-pack): cream card, overlapping jar renders, one button adds the set.
- Stat band (.s2-stats): flame, white numbers. Real numbers only.
- Ingredient tabs (.s2-inside): ink band, gold active tab, full label text.
- Legacy sections (spx-*) are restyled through assets/spx2.css overrides.

## Dos and don'ts
- Do use the real jar renders and the store's own lifestyle photos.
- Do keep every claim checkable (review counts come from Loox, ingredients from the labels).
- Don't promise notes in orders. Don't show WelcomeX or ADD2CART. FlavorX never applies to the Bundle.
- Don't use em dashes in copy.
- Don't add named customer quotes that are not real reviews.

## Motion philosophy
Small and quick. Buttons lift 1px, jars lift 4px on hover, the benefit ticker scrolls slowly. Everything stops under prefers-reduced-motion.

## Product page (v2, Nov 15)
Order: spx2-pdp (photo carousel on the blend color, name, one sentence, key facts, rating, one button, box offer), spx2-label (blend color card with lead ingredients, heat, uses, two label numbers, and the real nutrition panel), recipes, more flavors (color tiles), reviews (Loox), sticky add bar. No tabs and no FAQ on product pages. Every number comes from the jar's nutrition label.

## Copy rule
Every line states a fact, a price, an ingredient, or what to do next. No slogans.

## Voice (Nov 15)
Promise: healthy food that tastes like something you would order.  Proof: 0 calories and 0g sugar per serving, six flavors, 4.9 from 132 reviews, 120+ servings in every jar.
The customer is the hero of every line. Karim appears only on the About page as co-founder, never on product pages or the homepage. Second person, short, positive and benefit first, never a joke at the food or the customer. Lead with taste, then price, then ease. Health numbers are proof, not the headline. Always say "per serving" next to 0 calories or 0g sugar. No slogans, no label talk as a selling point, no em dashes.

## Standing rules from the owner (Nov 15)
- Guarantee wording is "30-day money back guarantee". Never say the customer keeps the jar and never mention return shipping.
- Nutrition panels shown on the site are cropped above the maker block. No barcode, no manufacturer name or address.
- No "60 formulations" stat or line anywhere.
- No "How Karim cooks it". Cooking tips speak to the customer ("Make it tonight").
- Price, savings and Checkout stay pinned under the header on the box builder.
- Product photography is studio grade. No jar pasted over an unrelated photo.
- Product photos never show an open lid, a hand, or seasoning being poured or shaken. Closed jar, standing upright, next to finished food.
- Cards and tiles on flavor colors use the jar renderings. Product page galleries use the real-jar studio and food photos.
- Model photos (Nov 15 shoots): the six color studio portraits run as the edge to edge wall under the homepage ticker and as the second photo on each product page. The six lifestyle portraits run as the scrolling cards after the how it works steps and as the fourth photo on each product page. They are brand photos with generated models. Never caption them as customers, reviews or testimonials.
- No calorie or sugar claims anywhere (owner, Nov 15): never say 0 calories, 0g sugar, zero sugar or anything like it, even though the label rounds to zero per 1/4 tsp. Several blends list sugar. Say where the sweetness comes from instead, and leave the numbers to the real nutrition panel. Product pages show servings per jar and the ingredient count.
- Scrolling banners (announcement bar and benefit ticker) repeat their list 12 and 8 times and move by exactly one list, so they loop with no gap on wide monitors.
- Older pages (Nov 15): cart and recipe pages keep their own sections but are restyled by the bridge block at the end of spx2.css. Search, contact, 404 and the About heading use spx2-search, spx2-contact, spx2-404 and spx2-pagehead. Policy pages are styled in spx2.css. layout/theme.liquid fills in a meta description when a page has none.
- Three audiences (owner, Nov 15): meal prep, weeknight dinners (easy and fast), and bored of bland (more flavor). Each has a landing page (page.meal-prep, page.weeknight, page.flavor) with its own hero, steps and starter set, and the homepage links to all three from the Built for how you cook section. Ads and emails for an audience go to its landing page.
- Brand headline (owner, Nov 15): "Crave what you cook." It replaces "Crave your homemade meals." everywhere. The meal prep page keeps its own version, "Crave your meal prep."
