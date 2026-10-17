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
