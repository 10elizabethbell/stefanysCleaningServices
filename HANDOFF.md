# Stefany's Cleaning Services LLC — handoff at ~60%

**Live:** https://10elizabethbell.github.io/stefanysCleaningServices/ · **Repo:** https://github.com/10elizabethbell/stefanysCleaningServices · **Built:** 2026-10-20 from Muse brief 2026-10-20 (NJ Small Business Network "Fall Calls for Extra Care" post) · **Call Sheet:** site set

## Biggest gap first: no phone, no email
The business publishes no phone or email anywhere. Every contact control (hero "Message us", the quote form, the floating circle, the closing link) goes to **Facebook Messenger** at `https://m.me/stefanycleaningservices` (checked: it resolves to the Page's message thread). When the owner gives a number, fill `CONFIG.PHONE` / `PHONE_DISPLAY` (and `TEXTS: false` if it doesn't take texts) at the top of the script: the header top-right number, footer number, and every contact button switch to text/call automatically. `CONFIG.EMAIL` adds the footer email (the only place it appears).

## What's built
- Single `index.html`, calm band style, bands alternating: paper header (logo mark + "Stefany's / Cleaning Services LLC" wordmark) → navy hero → paper "care" band with the "See us on Facebook" row → navy services rows → paper quote section (3 steps beside the form) → navy close "Fall calls for extra care." with the full logo on a white circle → deep textured footer.
- Palette from the logo: logo blue deepened to #0a5196 (hero, services, close), deep #0b2a4a, paper #f4f7fb, leaf green #8cc63f as the one accent (fills; text on it is navy; #3d6a10 when green is text on light). Form hover/focus outline is the logo blue #077dd4.
- Hero: plain textured navy (no photo, see below). Eyebrow "Fall cleaning", H1 "A fresh start for your Maplewood home." (bounces in letter by letter), the owner's own promise line, two buttons: Ask for a quote (scrolls to the form), Message us (Messenger). On desktop the logo sits in a smaller white circle to the right (fills the empty half; not in the original contract, drop it if you'd rather keep the logo to the close).
- Quote form: name (required), kind of cleaning chips, about your home, town. Submit composes a message, copies it to the clipboard, and opens Messenger with `?text=` prefilled; a box shows the message with Copy / Open Messenger buttons. Service rows pre-pick their chip.
- Floating message circle: hidden on the hero, shown below it, hidden over the form and over the closing "Message us" link; opens Messenger with a prefilled hello.
- After sending, the send button hides (the result box has its own Open Messenger), and any edit brings it back.
- Favicon/home-screen icon from the logo's arc-and-tools mark; og.png 1200×630 for the Facebook link preview.

## Assumptions I made
- **Area = Maplewood, NJ.** Not inferred: it's in their own Facebook page title ("Stefany Cleaning Services | Maplewood NJ"), which Muse couldn't read. No other towns listed; the close says "Nearby and not sure we come to you? Ask us."
- **Name spelling:** "Stefany's Cleaning Services LLC" (logo and ad caption), per the brief. Their Facebook page says "Stefany Cleaning Services".
- **Voice "we/our":** the flyer says "Our team takes care of the cleaning".
- **Services:** Home cleaning, Deep cleaning, Seasonal cleaning — from the brief's category line, not an itemised list from the owner.
- **Care copy** ("We clean your home like it's our own", "You're trusting us with the place you come home to...") is mine, built from their caption's words (extra attention, comfort, freshness, peace of mind). Owner should confirm.
- **How it works** steps ("Send us a message / We set a day together / Come home to clean") describe the Messenger flow; no process facts from the owner.
- No free-quote claim anywhere; the form's eyebrow just says "On Messenger".

## Placeholders and gaps
- No photos of their work. The flyer's bathroom is a design-template image (Canva-style), not their job, so it isn't used. Hero is the plain navy band for that reason. **Photos wanted** (before/afters especially): they'd go in the hero and a work section above the Facebook row.
- No reviews, prices, hours, years in business, insurance: none on the page.
- The Facebook row says "See us on Facebook" rather than your usual "Click to see more of our work", because the page timeline wasn't readable and there are no work photos on the site to promise "more" of. Switch the wording once you've seen the page has job photos.

## Questions for the owner
- A phone number (and does it take texts)? An email for the footer?
- Which towns do you cover besides Maplewood?
- What do you clean: houses, apartments, move-in/move-out, offices, Airbnbs? Do you bring supplies?
- Is it you alone or a team? Can we name you (Stefany) on the page?
- Any before/after photos and customer reviews we can use?
- Hours/days you work; insured?

## Ideas not built (yours to pick)
- **Runner-up worlds (opt-in signature motion):** 1) soap bubbles drifting up from the hero's bottom edge that pop on touch (best fit: cleaning product, matches the logo's spray bottles); 2) a squeegee wipe: drag across a misted hero to wipe it clear; 3) falling autumn leaves you sweep away (fits the fall promo); 4) sparkle stars from the logo twinkling where you touch.
- A move-in/move-out or holiday cleaning section once the owner confirms those services.
- Work photo cards (4:5) and before/after sliders once photos exist.
- Swap the hero to a real photo under the navy overlay once there's a usable one.
- **Impeccable findings kept because they're your calm-style choices:** eyebrow pills (craft floor bans them), the H1 bounce-in (animate/quieter dislike elastic easing), the floating circle, Cal Sans, the diagonal band texture (detector "repeating-stripes-gradient"; I added a narrow ignore in `.impeccable/config.json`), the same fade-up on every section.
- **Field fill contrast:** #e6ecf5 fields on the white card are 1.19:1 (WCAG 1.4.11 wants 3:1 for input edges). Kept borderless per the calm style; the labels identify each field. Darken or add a hairline if you want strict compliance.
- **Not taken from the reviews:** a ✓ glyph on selected chips (craft floor says no glyph icons; the navy fill already shows it), header shadow on scroll (the header doesn't stick, so nothing to shadow), merging `.lede`/`.promise` into one size token.
- Copy alternative for the hero: "Come home to clean in Maplewood." (shorter, but ambiguous).

## Not verified
- Messenger `?text=` prefill on real phones (inside the Facebook app and in Safari). If it opens empty, the message is already copied and the page says to paste it; check this on an iPhone and Android.
- Real-device touch, clipboard behaviour inside Facebook's in-app browser.
- Messenger requires the visitor to be logged in to Facebook; a logged-out desktop visitor lands on a login page.
