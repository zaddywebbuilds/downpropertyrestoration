# Dawn Property Restoration: research and handover

Prepared 17 October 2026. Everything below is what was actually verified, what was
inferred, and what the owner still has to confirm before this goes public.

## 1. What was verified

| Field | Value | Source |
|---|---|---|
| Business name | DAWN PROPERTY RESTORATION | Google Business Profile |
| Google category | **Real estate rental agency** | Google Business Profile |
| Address | 942 Howard Ave, Windsor, Ontario N9A 1S5, Canada | Google Business Profile |
| Coordinates | 42.3128356, -83.0262241 | Google Business Profile |
| Phone | +1 343-997-2126 | Google Business Profile |
| Hours | Open, closes 12:00 am | Google Business Profile |
| Website | None. Listing still shows "Add website" | Google Business Profile |
| Reviews | None. No star rating | Google Business Profile |
| Photos | 10 listed, 9 distinct (the cover is served twice) | Downloaded from the listing |

Listing URL: https://www.google.com/maps/place/DAWN+PROPERTY+RESTORATION/@42.3128356,-83.0262241,17z

## 2. The positioning question, and how it was settled

The name contains "Restoration", which reads as a disaster-restoration contractor
(water, fire, mould, storm). **The evidence does not support that reading.**

- Google's category for the business is *real estate rental agency*, not a
  restoration or contracting category. Categories are chosen by the owner.
- All 9 photos the owner uploaded show furnished bedrooms, a shared kitchen,
  tenant fridges, two lounges and bathrooms. None shows equipment, crews, PPE,
  damage, or any restoration work.
- Web searches for the business name, the address and the phone number returned
  nothing. There is no site, no social profile, no directory entry, no listing.

Most likely reading: they renovate ("restore") properties and rent them out by the
room. The name describes what they do to the building; the revenue is rental.

**Confirmed with the client contact on 17 Oct 2026: furnished room rentals.**
The site is built on that basis.

## 3. What the photos actually show

| File | Content |
|---|---|
| photo_001 | Bedroom: single bed with new mattress, side table, folding chair |
| photo_002 | Dining / common area: two tenant fridges, dining table, work table |
| photo_003 | Bathroom: tiled walk-in shower, glass block window, sink and mirror |
| photo_004 | Sitting room: rattan sofa set, coffee table, exterior door |
| photo_005 | Galley kitchen: gas range, microwave, large stainless fridge |
| photo_006 | Second sitting room: rattan seating, tiled floor, large windows |
| photo_007 | Separate toilet: fitted with a bidet sprayer |
| photo_008 | Bedroom: bed, desk and chair, blinded window |
| photo_009 | Dome security camera mounted at the ceiling |

Throughout: new vinyl plank flooring, fresh pale sage paint, new interior doors,
trim, blinds, ceiling fixtures and smoke alarms. The building has been renovated
recently and thoroughly.

## 4. What the site claims, and why

Every claim on the page is traceable to a photo or to the listing. Specifically:

- Furnished room with bed, mattress, desk, chair, blinds, overhead light, smoke alarm
- Fridge space per tenant in the common area
- Shared kitchen with gas range, oven, microwave, large fridge
- Two lounges and a dining table
- Tiled shower room, and a separate toilet with a bidet sprayer
- New floors, paint, doors, blinds throughout
- Camera covering the shared entry
- Address, phone and "enquiries answered until midnight" (from listing hours)

**Deliberately not claimed:** no price, no reviews or testimonials, no years in
business, no certifications, no insurance claims, no tenant counts, no named
staff, no service area beyond Windsor, no Wi-Fi, utilities or laundry. None of
these could be verified, so none appear.

## 5. What the owner must confirm before this is public

1. **Rate per room**, and whether it is weekly or monthly. The page has no price;
   adding one is the single biggest conversion improvement available.
2. **What the rate includes**: hydro, heat, water, internet, laundry. The page
   currently says "ask what the rate covers", which is honest but weak.
3. **Laundry**: is there a washer and dryer on site? Not visible in any photo.
4. **Internet**: included, extra, or tenant's own?
5. **Who the rooms are for**: students, workers, newcomers, any restriction.
6. **Lease terms**: minimum stay, deposit, first and last month.
7. **House rules**: guests, smoking, quiet hours, shared-space cleaning.
8. **How many rooms** exist and roughly how many are usually free.
9. **Correct business email**: there is none on the listing, and the enquiry form
   currently composes a message for the tenant to send by text rather than
   emailing anyone.
10. **Phone number**: 343 is an Ottawa-area code, not Windsor's 519/226/548.
    Worth confirming it is the right number for enquiries.
11. **Whether they also do restoration or renovation work for other owners.** If
    they do, that is a second service worth its own section, and the name finally
    makes sense to a visitor.

## 6. Build notes

- Source: `site/index.html`, single file, no build step, no framework.
- Images: `site/img/`, resized to 1800px long edge, quality 82, EXIF stripped
  (the originals carried camera metadata; GPS was removed with it). 2.4 MB total,
  down from 14 MB.
- Originals kept untouched in `images-google-maps/`.
- Fonts: Fraunces and Public Sans, loaded from Google Fonts.
- Palette is taken from the house itself: the sage the walls are painted.
- Accessibility: keyboard-reachable gallery, visible focus rings, labelled form
  fields, reduced-motion respected, alt text on every image.
- SEO: title, meta description, LocalBusiness schema with the verified address,
  phone and coordinates. No invented claims in the structured data.

## 7. Known limitations

- **The enquiry form does not send anything.** It composes a message the visitor
  copies and texts to the listed number. A real form needs an email address or a
  form endpoint, and a privacy notice once it collects personal data.
- **No before/after section.** The spec asked for one, but only "after" photos
  exist. Faking a "before" would misrepresent the property, so it was left out.
  If the owner has pre-renovation photos, this becomes the strongest section.
- **No exterior shot.** There is no photo of the building from the street, which
  a renter looking at a rooming house will want. Worth asking for.
- **Single page.** For one house with nine photos this is the right shape. Service
  pages would be mostly empty. If they add properties, it should become multi-page.

## 8. Deployment

Live at **https://zaddywebbuilds.github.io/downpropertyrestoration/**
(GitHub Pages, served from `main` at the repository root.)

Note the repository is spelled `downpropertyrestoration`. The business is
`Dawn`. Worth renaming before this URL is given to the owner or printed
anywhere, since "down property restoration" reads badly for a property business.

Render-checked headless at 1440px and 390px: no horizontal overflow at either
width, all 15 image references load, Cormorant Garamond and Inter both resolve,
and no console errors.

## 9. The AI image concept pack

A zip of 15 AI-generated restoration images was supplied
(`DAWN_Restoration_Image_Concept_Pack.zip`). **None of it was used**, for two
independent reasons.

**It is the wrong business.** The set covers water damage, fire and smoke,
mould remediation, storm damage and restoration equipment. This business rents
furnished rooms. Showing a prospective tenant a crew extracting floodwater
would not describe anything the company sells.

**It is technically unusable regardless of positioning.** The pack's own
README states the files are crops from a single contact sheet rather than
independent generations. Measured dimensions:

| File | Pixels | Needed |
|---|---|---|
| 01_homepage_hero | 930 x 317 | ~2400px wide for a hero |
| service images (02-11) | about 300 x 240 | ~1200px |
| 12_before_room | 180 x 252 | pair must match |
| 13_after_room | 158 x 252 | pair must match |

The before/after pair cannot drive a comparison slider: the two frames are
different aspect ratios, so they are not the same room from the same camera
position. `12_before_room.jpg` also has a vertical slice of a neighbouring
image bleeding in along its left edge, which is visible at full size.

The nine real photographs of the actual property are higher resolution
(1800px long edge), genuinely show what is being rented, and cost nothing in
credibility. They remain the better asset.

## 10. Revision 2

Changes after review:

- **Aesthetic** rebuilt on the Oasis Massage Studio reference the client gave:
  Cormorant Garamond over Inter, warm cream gradient ground, glass panels at
  28-40px radii, pill buttons, gold eyebrows, coral CTA, soft warm shadows.
- **No cropping.** All `object-fit: cover` and forced aspect ratios removed, so
  every photograph shows in full. The gallery is CSS columns so mixed portrait
  and landscape tile without gaps. The single portrait feature is width-capped
  rather than cropped.
- **Spacing tightened.** Section padding cut from a 7rem maximum to 3rem.
  Desktop page height fell from 12851px to 7227px, mobile 18066px to 9476px.
- **Images regraded and converted.** Brightness +8%, contrast +3%, applied
  uniformly. No white balance: grey-world would have stripped the sage wall
  colour, which is a real feature of the house. WebP added with JPEG fallback
  via `<picture>`, saving 49% (2511KB to 1281KB). Intrinsic width and height on
  every image to stop layout shift, lazy loading below the fold,
  `fetchpriority="high"` on the hero.
- **Availability section added** with the structure for rate, coverage, minimum
  stay, deposit and start date, each reading "Ask when you call" until the owner
  confirms real figures. An HTML comment marks the block for replacement.

Verified headless at 1440px and 390px: no horizontal overflow, 15/15 images
resolve, all served as WebP, no console errors.

### Still outstanding

- No real rate anywhere. Still the single biggest gap.
- Enquiry form composes a message for the visitor to send; it does not transmit.
  Needs the owner's email or a form endpoint, plus a privacy notice.
- No exterior photograph of the building.
- No pre-renovation photographs, so no before/after comparison is possible.

## 11. Revision 3

Each of the nine photographs now appears exactly once on the page. Previously
six of them ran twice, once in a section and again in the gallery.

Current placement, one photo per slot:

| Slot | Photo |
|---|---|
| Hero | 008 room with desk and bed |
| The room | 001 bedroom |
| Shared spaces | 005 kitchen, 004 first sitting room |
| Looked after | 003 tiled shower room |
| Gallery | 002 dining and fridges, 006 second sitting room, 007 separate toilet, 009 entry camera |

Desktop page height is now 6699px, down from 12851px before the spacing and
cropping work. Mobile is 9186px, down from 18066px.

## 12. Restoration imagery: what was used and what was not

The concept pack was integrated into the existing page as a labelled
"Restoration and renovation work" section, rather than a second page.

The rule applied: **images that show work can go on a rental page; images that
show a property cannot.** On a page letting a room, every photograph of a
building reads as the building you would be renting. An illustrative exterior
or a restored living room would imply that is the house, which no amount of
small print fixes.

### Used (7)

| File | Shown at | Native | Placement |
|---|---|---|---|
| hero-restoration | 930px | 930x317 | Section banner |
| water-damage | 282px | 305x233 | Service card |
| fire-smoke | 282px | 302x233 | Service card |
| mold-remediation | 282px | 305x233 | Service card |
| storm-damage | 282px | 297x233 | Service card |
| property-repairs | 282px | 299x233 | Service card |
| equipment | 282px | 266x252 | Service card |

Each is displayed at or below native width, so nothing is upscaled. On a high
density screen the banner will still look soft, because 930px native is 1x.

### Not used (8), with reasons

| File | Reason |
|---|---|
| residential-exterior | Depicts a property. Would be read as the rental. |
| commercial-exterior | Depicts a property, and no commercial offering is confirmed. |
| closing-cta | A restored interior. Would be read as a room on offer. |
| hero-exterior-alt | Same problem as residential-exterior. |
| commercial-restoration | Commercial service unconfirmed; duplicated the repairs card. |
| assessment | Weak at 240x252 next to the others; cut for consistency. |
| before-room | See below. |
| after-room | See below. |

### The before/after pair cannot be used

`before-room` is 180x252 and `after-room` is 158x252. Different aspect ratios,
so they are not one room photographed twice from a fixed position. A comparison
slider fed this pair either distorts the images or shows them misaligned.
`before-room` also carries a vertical slice of a neighbouring frame along its
left edge, visible at full size.

A working slider was built and then removed along with the separate page. It
can be restored in about ten minutes once a genuine matched pair exists: one
room, one camera position, two moments.

### If the owner confirms these services

Remove the "Proposed services, to confirm" badge and the caption beneath the
cards, and regenerate all six images individually at roughly 1200px wide. The
pack README states these are contact sheet crops, so regeneration is the
intended path, not upscaling.

## 13. Revision 4: layout density

- Section headings run as two columns on desktop, heading left and supporting
  line right, so the right half of each heading row is no longer empty.
- Band padding cut again, from a 3rem maximum to 2.3rem.
- The services banner and cards now stretch to the full container width.
- The FAQ panel fills the width; its answer text stays capped at 78 characters
  so lines remain readable.
- The hero caption card used to hang off the bottom-left corner of the photo,
  half on and half off. It now sits fully inside the frame, inset from the edges.

### Trade-off accepted

Filling the width upscales the concept images about 1.23x: the banner runs
930px native at 1148px, the service cards about 300px native at 371px. This was
the explicit choice over leaving visible dead space. It renders acceptably, and
regenerating those images at roughly 1200px wide removes the compromise.

**The nine photographs of the house are not upscaled.** They are 1350-1800px
native and never display above that.

## 14. Revision 5: gallery and hero

### Gallery now justified

CSS columns left a ragged bottom: one tall portrait stretched a column while the
others ended early. The gallery is now justified rows, where flex-grow and
flex-basis both scale with each image aspect ratio, so images in a row land on
the same height and the row ends flush. Nothing is cropped.

Desktop is one flush row of five. Phones use a smaller basis so it becomes two
rows of two plus a full-width last image, instead of a stack (too tall) or a
1 + 2 + 1 split (leaves a stub).

### Hero image changed, at the owner request

The hero is now img/hero-villa.jpg, cropped to 1200x800 from a portrait source.
The room photograph that used to be the hero moved into the gallery, so each of
the nine house photographs still appears exactly once.

**Provenance, recorded deliberately.** This image is not 942 Howard Ave. It
shows a modern hillside house with palm trees and an infinity pool, which does
not exist in Windsor, Ontario. The source file was
Downloads/pinvideosaver_l0ozs1sg.jpg, saved from Pinterest through a downloader,
so the copyright holder is unknown and no licence has been obtained.

Three concerns were raised before this change and the owner chose to proceed:

1. The hero slot reads as the property being rented.
2. Unknown rights holder, which is a licensing exposure on a commercial site.
3. Portrait source in a landscape slot, so it required the cropping that was
   otherwise ruled out.

To reverse it, point the hero picture element back at photo_008 and remove the
duplicate gallery figure.

The authenticity line was narrowed again to match: it now reads "Every
photograph of the rooms and shared spaces is of this building", which stays
true with a non-property hero. The Open Graph preview image is still the real
room photograph, not the villa.
