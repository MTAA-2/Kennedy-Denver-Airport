# Wage Justice Help — Denver Airport TSA Screening

Static GitHub Pages rebuild of https://wagejusticehelp.com/,
converted from the client's supplied file (`index-3dafe05c.html`,
"DEN TSA Page, Friendly") into our current framework format.
Built from the overtime Version A build
(`github-overtime-justice-help-landing-page/`), same firm, same
embed, recolored and re-laid-out for this version. HTML + CSS
only, no PHP.

## Subject

Denver International Airport restaurant and shop workers —
current or former — who must clear TSA security before they can
clock in. The claim is unpaid pre-shift time (TSA line,
screening, train or walk to the post) and, secondarily, missed
rest breaks and worked-through meal breaks. Colorado law only;
no other state, trade, or employer is named. This is a
different claim from the data-center overtime pages — no data
centers, no overtime premium.

## Framework carried over (unchanged)

- MTAA CIPA block script in the head
- Meta Pixel **1238664640565416** + ViewContent
- MTAA form embed **nf_3270a8a1b0e4425cb70e9f97f2fa5a3c** in the
  overflow form card (hangs past the hero, scrolls internally)
- Relative footer legal links (privacy-policy.html / disclaimer.html)

## Branding

- **Kennedy Law Firm, LLP**, 2925 Richmond Ave., Ste. 1200,
  Houston, TX 77098 — Galvin Kennedy responsible for the page
- Phone **713-425-6445** in the header and footer (the rendered
  sample displays it twice)
- Header carries the gold KENNEDY logo image, as on the sample
- Footer disclaimer is the sample's own four paragraphs, verbatim
  (including the "not affiliated with Denver International
  Airport, the TSA, or any employer" line)
- Verified: zero traces of the overtime build or the tobacco
  framework

## Palette — sampled live from the rendered page, 2026-11-20

Matches the client's file exactly:

| Surface | Color |
|---|---|
| Page / hero / footer background | sky blue `#eaf4ff` |
| Header / cards | white `#ffffff` |
| Headings / ink | navy `#1d2a44` |
| CTA buttons | sunny yellow `#ffd15c`, navy text (hover `#ffc93a`) |
| Eyebrow / kicker / title accents | teal `#0b666b` |
| Header / footer phone | teal `#0b666b` |
| Mint callout | `#e3f6ef` |
| Form rows (sample's native form) | pale blue `#dcecff` |
| Headline highlighter | yellow `#ffd15c`–`#ffe7a8` gradient |
| Step circles | yellow `#ffd15c` |

Headings use **Fredoka** (the sample's rounded display face);
body is **Nunito**. Buttons are full pills with the 4px
sun-deep (`#e9b322`) bottom edge, as on the sample. Section
headings carry no band on this sample, so the framework's band
was removed.

## Content — kept to what this version actually has

In the sample's order:

1. Hero: "Denver Airport Restaurant and Shop Workers: Unpaid
   TSA Screening?" with the yellow highlight, the subhead, the
   "5 quick taps / About 2 minutes" badges, and the form card
   beside it
2. "Your shift starts in the security line" — the journey card
   with the four-stop path (TSA line / Screening / Train or
   walk — each "unpaid?" — then Clock in, "paid"), the mint
   "Colorado law might treat security screening as paid time."
   callout, and the breaks aside ("Missed rest breaks or worked
   through lunch? There is a spot for that on the form too.")
3. "What happens next" — the same three steps as white cards
   with yellow number circles

No FAQ, no qualify cards, no closing CTA section — this version
has none, so neither does this build.

The five-question form (worked at a DEN restaurant or shop?;
when started; how paid; unpaid time before clock-in — TSA line,
screening, walk, train; break problems — rest breaks, meal
breaks, pay deducted) plus contact, employer, and consent is the
sample's native form, replaced here by our MTAA embed, as on the
overtime builds.

## CSS changes vs the overtime Version A build

Colors and heading/body font-family values only, plus the
sample's components the framework has no rule for (grouped in
the marked block at the end of style.css): the hero fee line,
the journey card with its four-stop path, the breaks aside, and
the step cards with titles. Two deliberate departures from a
pure color swap, both driven by the sample: the section-title
band is removed (this sample's headings carry none), and the
eyebrow/kicker/title-accent text uses the sample's teal instead
of the yellow action color, which is unreadable as text. The
hero renders flat sky blue — the sample has no hero photo, so
the parallax class is off the hero and its rule points at the
usual placeholder. Diff-verified.

## Placeholders — one file to drop in

- **`KENNEDY-logo.webp`** — the gold logo image, referenced in
  the header and footer (same file as the overtime builds).
  Drop it into this folder's root.

There is no hero-photo placeholder: the sample has no hero
image. The other parallax bands point at `YOUR-IMAGE-URL-HERE`
(unused on this page's sections, kept from the framework).

## Flags

- **The fee line comes from the live page, not the file.**
  The rendered hero carries "If you're a fit, we'll pay to look
  into your case — no fee unless you win." — the supplied file
  has no fee language anywhere. It is included in the hero as
  rendered live. This is the first Kennedy page with fee
  language; the overtime pages had none.
- **The sample's own form has an empty lead endpoint**, same as
  both overtime versions (`leadEndpoint: ""`). This build uses
  our MTAA embed instead, so leads flow normally.
- **The sample has no legal links at all** — no Privacy Policy,
  Disclaimer, or Terms links anywhere on the page. The
  framework's relative privacy-policy.html / disclaimer.html
  links are kept (his own pages). (The file also flags its own
  privacy URL as "not set.")
- **Pixel:** the client's file carries its own pixel
  (249210042119489). This build keeps our framework pixel; swap
  the two `fbq('init', ...)` / noscript lines if this campaign
  runs on the client's pixel instead.
- **Form questions verified from the file only.** The live page
  shows only Question 1 until it is answered (per the no-submit
  inspection rule); questions 2–5, contact fields, and consent
  text are taken from the supplied file, and Q1 matches it
  exactly.
