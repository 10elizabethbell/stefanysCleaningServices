---
name: Stefany's Cleaning Services LLC
description: A calm, logo-coloured band site that turns a Facebook-only Maplewood cleaner into a Messenger quote.
colors:
  paper: "#f4f7fb"
  card: "#ffffff"
  field: "#e6ecf5"
  ink: "#0b2a4a"
  body: "#253a52"
  soft: "#4a5b6e"
  navy: "#0a5196"
  deep: "#0b2a4a"
  on-dark: "#f4f7fb"
  on-dark-soft: "#cddcee"
  green: "#8cc63f"
  green-2: "#a0d35a"
  green-ink: "#3d6a10"
  focus: "#077dd4"
  error: "#b3261e"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, min(12vw, 15svh), 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(22px, 6vw, 28px)"
    fontWeight: 400
    lineHeight: 1.15
  title-sm:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.2
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 19px)"
    fontWeight: 400
    lineHeight: 1.7
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.4
rounded:
  field: "10px"
  card: "24px"
  pill: "999px"
spacing:
  gutter: "20px"
  gutter-desktop: "40px"
  section: "64px"
  section-desktop: "96px"
  column-gap: "64px"
  wrap: "1160px"
components:
  button-primary:
    backgroundColor: "{colors.green}"
    textColor: "{colors.ink}"
    typography: "{typography.title-sm}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.green-2}"
    textColor: "{colors.ink}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    typography: "{typography.title-sm}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-small:
    backgroundColor: "{colors.card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 20px"
    height: "48px"
  input-field:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.card}"
  form-card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "clamp(20px, 5vw, 32px)"
  service-row:
    textColor: "{colors.on-dark}"
    typography: "{typography.title}"
    height: "76px"
  link-card:
    backgroundColor: "{colors.card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    height: "76px"
  arrow-circle:
    backgroundColor: "rgba(11,42,74,.07)"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "44px"
  arrow-circle-on-navy:
    backgroundColor: "rgba(255,255,255,.12)"
    textColor: "{colors.on-dark}"
  arrow-circle-hover:
    backgroundColor: "{colors.green}"
    textColor: "{colors.ink}"
  logo-circle:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.pill}"
    width: "min(220px, 58vw)"
  float-circle:
    backgroundColor: "{colors.green}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "60px"
---

# Design System: Stefany's Cleaning Services LLC

## Overview

**Creative North Star: "The Fresh-Start Band"**

The site is the logo, laid out flat as full-bleed bands. Off-white paper and two blues taken from the logo's arc alternate down the page so every section change is obvious on a phone, and the logo's leaf green is the one accent: it fills the things you press and nothing else. There are no photos (the business has no real work photos), so the depth comes from the colour of the bands, a faint diagonal line texture on the hero and footer, and two white objects that sit on the blue: the quote form card and the logo on its white circle.

The density is phone-first and generous: one column, 64px between bands on phones and 96px on desktop, big tap targets (44px minimum, 56px for main buttons), and only one control of each kind in view at a time. Headings are Cal Sans at a single weight; everything you read is the system stack at 16/1.7. Motion is spent in two places: the hero H1 bounces in letter by letter, and content below the first screen rises 12px into place once. Nothing else moves.

The system follows the owner's house calm band style (`~/.claude/skills/pitch-site/references/calm-photo-style.md`), with the logo's green standing in for that style's usual warm gold accent.

**Key Characteristics:**
- Full-bleed bands in a fixed order: paper header, navy textured hero, paper, navy, paper, navy, deep textured footer.
- One accent (leaf green) used as a fill; a darker green only when green has to be text on paper.
- Cal Sans display at weight 400 only, system body at 16/1.7.
- Soft, borderless shapes: 24px cards, 10px fields, full pills, circles.
- Links that are whole rows; the only thing that changes on hover is a 44px arrow circle.
- One contact channel at a time, switched from a single CONFIG block.

## Colors

Paper and two logo blues carry the page; leaf green is the only accent and it is a fill, not a text colour.

### Primary
- **Logo Navy** (`navy`): the hero, the services band and the close band. It is the logo's brand blue deepened so white and green both read on it. Carries the diagonal texture on the hero only.
- **Night Navy** (`deep`): the footer, always with the diagonal texture. Same value as `ink`; kept as its own token because its role (a band ground) differs from ink (a text colour).

### Secondary
- **Leaf Green** (`green`): primary button fill, the floating message circle, the step-number circles, the eyebrow dot, arrow circles on hover, and `::selection`. On navy bands and the hero it may also colour the last phrase of a heading (large text only). Text on a green fill is always `ink`.
- **Spring Green** (`green-2`): the primary button's hover fill. Nowhere else.
- **Leaf Green Ink** (`green-ink`): green as text or icon on paper (5.7:1), e.g. the heading accent phrase on paper and the header phone icon.

### Tertiary
- **Logo Blue** (`focus`): the logo's own brand blue, used only as the focus and form-hover outline on light grounds, so focus never looks like the green fill.

### Neutral
- **Morning Paper** (`paper`): page ground, header, and the light bands. Also `on-dark`, the heading colour on navy.
- **Clean White** (`card`): the quote form card, the Facebook link card, the logo circle, the small outlined buttons.
- **Rinse Blue** (`field`): fill for inputs, chips and the "message ready" box on the white form card (it must stay visibly darker than the card; paper on white failed 1.4.11).
- **Ink Navy** (`ink`): headings on paper, button text on green, the selected chip fill.
- **Slate Body** (`body`): running text on paper.
- **Soft Slate** (`soft`): ledes, step descriptions, helper text and the wordmark's "Cleaning Services LLC" line on paper.
- **Mist Blue** (`on-dark-soft`): running text on navy and in the footer.
- **Error Red** (`error`): the inline error sentence and the error border on a field. Used only by the form.

### Named Rules
**The Fill-Only Green Rule.** Leaf green (`green`) is a fill. On paper it never appears as text; use `green-ink`. On navy it may be text only at heading size.

**The Band Contrast Rule.** Bands alternate light and dark so a new section is obvious; two navy bands are never adjacent, and every navy band is followed by paper or the deep footer.

## Typography

**Display Font:** Cal Sans (Google Fonts, `display=swap`), with Avenir Next, Segoe UI, system-ui
**Body Font:** the system stack (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial)

**Character:** A friendly geometric display face at one weight against the phone's own text face. Cal Sans also sets everything you tap (buttons, service rows, the Facebook row, form labels, the wordmark), so the clickable layer reads in the brand voice while explanations stay plain.

### Hierarchy
- **Display** (400, clamp 42px to 80px with a 15svh cap, 1.02): the hero H1 only, white, max 12ch, with the place in it.
- **Headline** (400, clamp 30px to 48px, 1.08): each band's H2, balanced wrapping.
- **Title** (400, clamp 22px to 28px, 1.15): service rows on navy. The closing "Message us" link steps up to clamp 24px to 36px.
- **Title Small** (400, 18px to 21px, 1.2): buttons (18px), form labels and legends (18px), step titles and step numbers (20px), the Facebook row (clamp 18px to 21px), the wordmark "Stefany's" (21px, 24px on desktop).
- **Lede** (system, clamp 17px to 19px, 1.7, max 38ch): the paragraph under a band heading. The hero promise is the same family at clamp 17px to 20px, line-height 1.5, max 32ch (40ch on desktop).
- **Body** (system, 16px, 1.7): running text, inputs (never under 16px, so iOS does not zoom), footer.
- **Label** (system, 14px): "(optional)" hints, the inline error, the line under the send button.

### Named Rules
**The One Weight Rule.** Cal Sans is used at 400 only. Hierarchy comes from size and colour, never from bolding the display face.

**The Tappable Voice Rule.** If it is a link or a button, it is set in Cal Sans. If it explains, it is in the system face.

## Layout

A single centred column (max 1160px) with a 20px gutter on phones and 40px from 760px up. Bands pad 64px top and bottom on phones and 96px from 760px; the hero uses 56/68px on phones and 96/112px on desktop. Band intros (`head`) stack eyebrow, heading and lede at 16px gaps, max 640px wide.

Breakpoints: 760px (desktop spacing, side-by-side hero buttons at min 230px each, larger header) and 1024px (two-column layouts). At 1024px the services band and the quote band become two columns (1fr / 1.2fr, 64px gap); the quote band's intro and steps stick at 40px from the top while the form scrolls. The close band becomes text plus logo circle. The hero gains the logo circle on the right, vertically centred, 200px to 250px. A 380px rule tightens chip padding on the smallest phones.

Band order for this site: paper header, navy textured hero, paper "care" with the Facebook row, navy services, paper quote (intro, three steps, form), navy close with the logo circle, deep textured footer. The footer pads its bottom by 96px plus the safe area so the floating circle never covers its links.

## Elevation & Depth

Depth is mostly tonal: dark and light bands, and white objects set on them. Shadows are rare, soft and ambient, tinted with the ink navy, and only on the few white objects that sit on paper, plus the floating circle that sits over everything.

### Shadow Vocabulary
- **Card lift** (`box-shadow: 0 8px 24px rgba(11,42,74,.07)` on the Facebook row, `0 10px 30px rgba(11,42,74,.06)` on the form card): just enough to lift a white card off paper.
- **Float** (`box-shadow: 0 10px 28px rgba(5,24,46,.3)`): the floating message circle only, because it rides over every band.

### Named Rules
**The Flat Band Rule.** Bands, rows, buttons, chips and inputs carry no shadow. A shadow means "a white object resting on the page", nothing else.

**The Quiet Texture Rule.** The diagonal texture (`repeating-linear-gradient(135deg, transparent 0 22px, rgba(255,255,255,.035) 22px 23px)`) appears only on the hero and the footer, and never above about 4% white, so it can never read as lines through text.

## Shapes

Soft and borderless. Fields are gently rounded (10px), cards are generously rounded (24px), and anything pressable that is not a field is a full pill or a circle: buttons, chips, arrow circles, step numbers, the floating circle, and the logo's white circle. Borders appear only as state (a 2px transparent border that turns blue on hover/focus or red on error) and as the 1px divider between service rows on navy (`rgba(255,255,255,.14)`). The brand mark is the logo's own arc-and-tools image; the full logo always sits on a white circle at 70% of the circle's width.

## Components

### Buttons
Big, round and sure of themselves.
- **Shape:** full pill (999px), 56px tall, 26px side padding, Cal Sans 18px, 20px icon with a 10px gap.
- **Primary:** green fill, ink text. One per view; it is the quote action.
- **Hover / Focus:** primary hover moves to spring green; inside the form the primary and small buttons also get a 3px logo-blue outline offset 3px on hover and focus. All buttons press to `scale(.98)`. Hover styles exist only under `(hover:hover)` so taps never leave them stuck.
- **Ghost:** transparent with a 2px 70%-white border, on navy only; hover goes to a solid white border and a 10% white wash. It carries the Messenger (or text) action next to the primary in the hero.
- **Small:** 48px, white with a 2px ink border; used for "Copy message" and "Open Messenger" in the sent box.

### Chips
- **Style:** pill, 48px tall, rinse-blue fill, ink 16px system text, 2px transparent border. The radio input is visually hidden but focusable.
- **State:** hover gives a logo-blue border; checked fills ink with white text; keyboard focus is a 3px outline offset 3px (a border would vanish on the ink fill). Tapping a service row pre-selects the matching chip.

### Cards / Containers
- **Corner Style:** 24px.
- **Background:** white on paper.
- **Shadow Strategy:** card lift (see Elevation & Depth).
- **Border:** none.
- **Internal Padding:** clamp(20px, 5vw, 32px) on the form card, 22px gaps between fields, max 600px wide.

### Inputs / Fields
- **Style:** rinse-blue fill, no visible border (2px transparent), 10px radius, 52px min height (textarea 110px, vertical resize), ink text, navy caret, 16px.
- **Focus:** the border turns logo blue; hover does the same on pointer devices.
- **Error:** a red border plus a plain-sentence error line under the field, wired with `aria-invalid` and `aria-describedby`; the rule is more specific than focus so the red survives focus.

### Navigation
The header is slim paper, 68px tall (80px on desktop): mark plus two-line wordmark on the left ("Stefany's" in Cal Sans over "CLEANING SERVICES LLC" in 12px uppercase system at .06em tracking), and the tap-to-call number on the right only once a phone exists. There is no menu. The footer is deep textured navy with the name, area, Facebook, and phone/email when configured, each link 44px tall, green on hover.

### Service Row (signature)
On navy, each service is a full-width link: the name in Cal Sans 22px to 28px on the left, a 44px arrow circle (12% white) on the right, 76px tall, separated by 14%-white hairlines. On hover or focus only the arrow changes: it fills green with ink arrow. The row itself never highlights, underlines or shifts. The Facebook row on paper is the same pattern as a white card: Facebook logo, label, arrow circle.

### Quote Form with Messenger Handoff (signature)
Name (required), kind-of-cleaning chips, "About your home", and town, then one full-width green "Send this on Messenger" button. Submitting composes a ready-written message, copies it, and opens Messenger; the button is replaced by a rinse-blue box (16px radius) showing the message with "Copy message" and "Open Messenger". Editing the form brings the button back. A line under the button says what will happen.

### Contact Switch (CONFIG)
Every contact control carries `data-contact` and reads one CONFIG block. With `PHONE` empty, all of them (hero ghost button, close "Message us", floating circle, form) go to `m.me/stefanycleaningservices` with a pre-filled message. Filling `PHONE` (and `PHONE_DISPLAY`) switches every one to `sms:` with the message body and relabels them "Text us"; `TEXTS:false` makes them `tel:` and "Call us". The header number and footer number appear only then. `EMAIL` appears only in the footer. `FLOAT:false` removes the floating circle. Visual treatment does not change between channels; only labels and destinations do.

### Floating Message Circle
A single 60px green circle, bottom right inside the safe area, with the float shadow. It slides up from 120px below (`.35s cubic-bezier(.2,.8,.2,1)`) once the hero has scrolled away, and hides while the quote form or the closing "Message us" link is on screen, so two of the same control are never in view. When hidden it is `tabIndex=-1` and `aria-hidden`. Hidden in print.

### Close Band and Logo Circle
Navy band: eyebrow with the business name, the seasonal H2 with its last phrase in green, a short paragraph, and a large Cal Sans "Message us" link with a green message icon (green text on hover). Beside it on desktop (below on phones, 160px), the full logo on a white circle.

### Motion
- **Hero H1 bounce-in:** JS splits the hero H1 into letters inside no-wrap word spans; each letter goes from `opacity:0; translateX(50px)` to rest over `1s cubic-bezier(.34,1.56,.64,1)`, staggered 20ms. It waits up to 600ms for Cal Sans so the swap can't jolt it, then restores the original H1 HTML on the last letter's `animationend`. The H1 carries an `aria-label` while split. Hero H1 only.
- **Fade-up:** elements marked to rise move 12px and fade in over .4s ease-out, and only if they start below the first screen. Everything is visible at rest, without JS, and in print.
- **Reduced motion:** no split, no fade-up, no float slide, no button transitions, no smooth scroll; the plain H1 shows at once.

### Eyebrow Pill (owner exception)
A deliberate owner choice from the house style, kept against the Impeccable craft floor and noted in HANDOFF.md. It is not a default to spread: it sits above the hero H1 and at most a few band headings (four on this page), is a `<p>` never a heading, 14px system 500 weight with .02em tracking, a 7px green dot, a faint ink (6%) or white (12%) wash, pill shape, and no arrow, hover, shadow or full green fill, so it can never be mistaken for a button.

## Do's and Don'ts

### Do:
- **Do** take every colour from the logo: paper ground, logo navy and night navy bands, leaf green as the one accent.
- **Do** put text on green in ink navy, and use `green-ink` (#3d6a10) whenever green must be text on paper.
- **Do** alternate light and dark full-bleed bands, with the diagonal texture only on the hero and the footer at 3.5% white.
- **Do** set every link and button in Cal Sans 400 and every explanation in the system face at 16px/1.7.
- **Do** make list links whole rows where only the 44px arrow circle changes on hover or focus.
- **Do** keep tap targets at 44px or more (56px for main buttons, 48px for chips and small buttons).
- **Do** route every contact control through CONFIG and `data-contact`, so Messenger and text/call switch together.
- **Do** keep the floating circle hidden while the form or the closing message link is on screen.
- **Do** use a logo-blue outline for focus on light grounds and a green outline on navy, hero and footer.

### Don't:
- **Don't** use green as text on paper, or white text on green.
- **Don't** add photos that are not the business's real work; the flyer's template bathroom stays out.
- **Don't** give bands, rows, chips or buttons a shadow; shadows are for white cards on paper and the floating circle.
- **Don't** animate any heading other than the hero H1, and don't add motion beyond the one 12px fade-up.
- **Don't** add a bottom contact bar or a second floating control; the floating circle is the only one.
- **Don't** put a phone number, email or towns list in the design before the owner supplies them; the slots stay hidden until CONFIG is filled.
- **Don't** add eyebrows beyond the hero and a few key headings, or give one an arrow, hover state or full green fill.
